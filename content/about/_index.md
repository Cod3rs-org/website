---
title: "About"
description: "Learn more about the Cod3rs Community and our mission"
---

{{< section id="basic-section" >}}

# About Cod3rs Community

Cod3rs Community is a diverse group of developers, designers, and tech enthusiasts who share a passion for coding and technology. 
We believe in the power of collaboration and knowledge sharing to create innovative solutions.

## Our Purpose

The Cod3rs Community exists to create a supportive environment where developers of all skill levels can learn, collaborate, and grow together. We focus on practical coding skills, project collaboration, and knowledge exchange. This is not just a theoretical discussion forum - we build real projects together!

## Our Goals

- **Learning Together**: We aim to foster a culture of continuous learning where members can enhance their coding skills through hands-on projects and peer support.
- **Building Projects**: We create meaningful open-source projects that solve real problems while providing learning opportunities.
- **Community Support**: We provide a welcoming space for both beginners and experienced developers to connect, share knowledge, and overcome coding challenges together.

## What We Do

### Technologies & Focus Areas
Our community works with a wide range of technologies, including but not limited to:
- Web Development (HTML, CSS, JavaScript, React, Vue, Angular)
- Backend Development (Node.js, Python, Java, PHP)
- Mobile App Development
- DevOps practices and tools
- Emerging technologies and frameworks

### Activities
- Collaborative coding sessions
- Code reviews and pair programming
- Open-source project contributions
- Knowledge-sharing workshops and presentations
- Hackathons and coding challenges

## How to Participate

### Community Platforms
While our primary meeting place is Discord, we also collaborate through GitHub and other platforms for our projects.

### Who Can Join
We welcome anyone with an interest in coding and technology, regardless of experience level. Whether you're just starting your coding journey or you're a seasoned professional, there's a place for you in our community.

### Requirements
- A positive attitude and willingness to learn
- Respect for all community members
- Adherence to our code of conduct
- Desire to participate and contribute to our collaborative environment

**Join us on this exciting journey of collaboration, innovation, and growth!**

{{< /section >}}

{{< rawhtml >}}
</div>

<div class="position-relative w-100 m-0">
    <div class="position-absolute m-5 px-3 rubik-mono-one-regular" style="z-index: 10">
        <p class="responsive-text">
            <span class="stroke-text">Now in</span>
            <span class="accent-color">Denmark</span><br>
            <span class="stroke-text">and</span> <span class="accent-color">Slovakia</span>
        </p>
    </div>
    <div id="chartdiv"></div>
</div>

<script src="https://cdn.amcharts.com/lib/5/index.js"></script>
<script src="https://cdn.amcharts.com/lib/5/map.js"></script>
<script src="https://cdn.amcharts.com/lib/5/geodata/worldLow.js"></script>
<script src="https://cdn.amcharts.com/lib/5/themes/Animated.js"></script>

<script>
    function spinSVG() {
        const svg = document.getElementById('spinning-svg');
        svg.style.transform = 'rotate(0deg)';
        svg.style.transition = 'transform 1s ease-in-out';
        
        setTimeout(() => {
            svg.style.transform = 'rotate(360deg)';
        }, 50);
    }
    var root = am5.Root.new("chartdiv");

    root.setThemes([
        am5themes_Animated.new(root)
    ]);

    var chart = root.container.children.push(am5map.MapChart.new(root, {
        panX: false,
        panY: false,
        wheelX: "none",
        wheelY: "none",
        projection: am5map.geoOrthographic(),
        paddingBottom: 20,
        paddingTop: 20,
        paddingLeft: 20,
        paddingRight: 20,
        rotationX: -10,
        rotationY: -55,
        zoomLevel: 7,
        maxZoomLevel: 7,
        minZoomLevel: 7
    }));

    var polygonSeries = chart.series.push(am5map.MapPolygonSeries.new(root, {
        geoJSON: am5geodata_worldLow 
    }));

    polygonSeries.mapPolygons.template.setAll({
        toggleKey: "active",
        interactive: true,
        fill: am5.color("#212121"),
        stroke: am5.color("#755AFB")
    });

    polygonSeries.mapPolygons.template.states.create("hover", {
        fill: am5.color("#755AFB")
    });
    
    polygonSeries.mapPolygons.template.states.create("active", {
        fill: am5.color("#755AFB")
    });

    var backgroundSeries = chart.series.push(am5map.MapPolygonSeries.new(root, {}));
    backgroundSeries.mapPolygons.template.setAll({
        fill: am5.color("#000000"),
        fillOpacity: 0.1,
        strokeOpacity: 0
    });

    backgroundSeries.data.push({
        geometry: am5map.getGeoRectangle(90, 180, -90, -180)
    });

    var graticuleSeries = chart.series.unshift(
        am5map.GraticuleSeries.new(root, {
            step: 10
        })
    );

    graticuleSeries.mapLines.template.set("strokeOpacity", 0.1);
    
    var alwaysActiveCountries = ["DK", "SK"]; // Denmark and Slovakia
    var previousPolygon;

    polygonSeries.mapPolygons.template.adapters.add("tooltipText", function(_, target) {
        const id = target.dataItem?.get("id");
        return (alwaysActiveCountries.includes(id)) ? "{name}" : "";
    });

    polygonSeries.mapPolygons.template.on("active", function(active, target) {
        const id = target.dataItem.get("id");

        if (alwaysActiveCountries.includes(id)) {
            target.set("active", true);
            return;
        } else target.set("active", false);
        
        if (alwaysActiveCountries.includes(id)) 
            previousPolygon = target;
    });

    function selectCountry(id) {
        var dataItem = polygonSeries.getDataItemById(id);
        var target = dataItem.get("mapPolygon");
        if (target) {
            var centroid = target.geoCentroid();
            if (centroid) {
                chart.animate({ key: "rotationX", to: -centroid.longitude, duration: 1500, easing: am5.ease.inOut(am5.ease.cubic) });
                chart.animate({ key: "rotationY", to: -centroid.latitude, duration: 1500, easing: am5.ease.inOut(am5.ease.cubic) });
            }
        }
    }

    polygonSeries.events.on("datavalidated", function () {
        alwaysActiveCountries.forEach((countryId) => {
            const dataItem = polygonSeries.getDataItemById(countryId);
            if (dataItem) {
                const polygon = dataItem.get("mapPolygon");
                if (polygon) {
                    polygon.set("active", true);
                    polygon.states.lookup("active").apply();
                }
            }
        });
    });
    chart.appear(1000, 100);
</script>

{{< /rawhtml >}}
