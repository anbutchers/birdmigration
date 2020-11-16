<!DOCTYPE html>
<meta charset="utf-8">
<link rel="shortcut icon" href="#" />

<head>
	<!-- add title -->
	<title>Bird Migrations Across North and South America</title>
	
    <!-- import required libraries here -->
	<script type="text/javascript" src="../lib/d3.v5.min.js"></script>
	<script type="text/javascript" src="../lib/d3-dsv.min.js"></script>
	<script type="text/javascript" src="../lib/d3-tip.min.js"></script>
	<script type="text/javascript" src="../lib/d3-legend.min.js"></script>
	<script type="text/javascript" src="../lib/topojson.v2.min.js"></script>
	<script type="text/javascript" src="../lib/d3-geo-projection.v2.min.js"></script>
	<style>
		<!-- define CSS rules here --> 
		.names {
			fill: none;
			stroke: #fff;
			stroke-linejoin: round;
		}
		
		.svg-content-responsive {
			display: inline-block;
			position: absolute;
			top: 100px;
			left: 100px;
		}
		
		<!--.graticule {
			fill: none;
			stroke: black;
			stroke-width: .5px;
			stroke-opacity: .5;
		}-->
	</style>
</head>

<body>
    <!-- Add heading for the visualization -->
	<div id="heading"></div>

	<!-- append visualization svg to this div-->
    <div id="choropleth"></div>

    <script>
	
		// enter code to define margin and dimensions for svg
		var w = 1500;
		var h = 700;
		
		//zoom settings
		const zoom = d3.zoom()
		.scaleExtent([0.5, 10])
		.on('zoom', zoomed);
		
		// enter code to create svg
		var svg = d3.select("#choropleth").append("svg")
		.attr("preserveAspectRatio", "xMinYMin meet").attr("viewBox", "0 0 1500 900")
		//.attr("width", w).attr("height", h)
		// Class to make it responsive.
		.classed("svg-content-responsive", true).attr("width", "100%").attr("height", "100%");
		
		var gw = 1384.35 - (1384.35 / 36.0)
		var gh = 693.183 - (693.183 / 18.0)
		
		var svg1 = svg.append("svg").attr("width", gw + 1).attr("height", gh + 1)
		// enter code to define projection and path required for Choropleth
		const projection = d3.geoEquirectangular()//.fitExtent([0, 0], [w, h])
		.scale(220)
		.translate([692.6749999999998, 347.0914981877568])
		
		const path = d3.geoPath().projection(projection);
		
		var g = svg1.append("g");
		
		var graticule = d3.geoGraticule()
		
		//grid settings
		var x = d3.scaleLinear()
		.range([0, gw]);

		var y = d3.scaleLinear()
		.range([0, gh]);

		var xAxis = d3.axisBottom(x)
		.ticks((w + 2) / (h + 2) * 10)
		.tickSize(h)
		.tickPadding(8 - h);

		var yAxis = d3.axisRight(y)
		.ticks(10)
		.tickSize(w)
		.tickPadding(8 - w);
		
		var gX, gY

		svg.call(zoom);
		
		//data for sample elements
		var dotSpot = [[-70,70], [-80,80]];
		//console.log(projection(dotSpot[0])[0])
		
		// define any other global variables 
		var promise1 = d3.json("custom.geo.json");
		// placeholder for bird data
		/*var promise2 = d3.dsv(",", "ratings-by-country.csv", function(d) {
			return{
				game: d.Game,
				country: d.Country,
				userNum: +d["Number of Users"],
				average_rating: +d["Average Rating"]
			}
		});*/

        Promise.all([
            // enter code to read files
			promise1 //, promise2 //uncomment this when bird data is defined
			
        ]).then(
            // enter code to call ready() with required arguments
			d => ready(null, d[0], d[1])
        );
		
		// this function should be called once the data from files have been read
		// world: topojson from custom.geo.json
		// replace gameData with birdData
		
        function ready(error, world, gameData) {			
			var Xcoordinates = graticule.lines().map(function (d) {
				var c = d.coordinates;
				return c[0][0];
			})
			
			var Ycoordinates = graticule.lines().map(function (d) {
				var c = d.coordinates;
				return c[0][1];
			})
			
			x.domain([d3.min(Xcoordinates), d3.max(Xcoordinates)])
			y.domain([d3.min(Ycoordinates), d3.max(Ycoordinates)])
			
			g.append("g")
			.attr("class", "countries")
			.selectAll("path")
			.data(world.features)
			.enter().append("path")
			.attr("d", path)
			.style("fill", "gray") //modify this to change map color
			.style("stroke", "white")
			.style("stroke-width", 0.3)
			
			/*g.append("path")
			.datum(graticule)
			.attr("class", "graticule")
			.attr("d", path);*/
			
			//circles to test interactivity features
			g.selectAll("circle")
			.data(dotSpot).enter()
			.append("circle")
			.attr("cx", function (d,i) { return projection(d)[0]; })
			.attr("cy", function (d,i) { return projection(d)[1]; })
			.attr("r", "3px")
			.style("fill", "red");
			
			//grid
			gX = svg1.append("g")
			.attr("class", "axis axis--x")
			.call(xAxis);
			
			gY = svg1.append("g")
			.attr("class", "axis axis--y")
			.call(yAxis);
		
		}
		
		function zoomed() {
			gX.call(xAxis.scale(d3.event.transform.rescaleX(x)));
			gY.call(yAxis.scale(d3.event.transform.rescaleY(y)));
			g.attr('transform', d3.event.transform);
		}
		
		var heading = d3.select("#heading");
		heading.append("text")
		.attr("transform", "translate (0, 0)")
		.style("font-size", "25px") 
		.style("font-weight", "bold")
		.text("Bird Migrations Across North and South America");
    </script>

</body>

</html>
