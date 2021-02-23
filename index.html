<!DOCTYPE html>
<meta charset="utf-8">
<style>

.links line {
  stroke: #999;
  stroke-opacity: 0.6;
}

.nodes circle {
  stroke: rgb(206, 102, 16)	;
  stroke-width: 1px;
  fill: black
}

svg {
  border:1px solid black;
}
</style>
<svg width="800" height="200"></svg>
<script src="https://d3js.org/d3.v4.min.js"></script>
<script>
//create somewhere to put the force directed graph
var svg = d3.select("svg"),
    width = +svg.attr("width"),
    height = +svg.attr("height");
    
var radius = 15; 

var nodes_data =  [];
var numNodes = 100;
for(i = 0; i < numNodes; i++){
    nodes_data.push({"id": "Kreis"});
}

//Sample links data 
//type: A for Ally, E for Enemy

var nodes = d3.range(numNodes).map(function(d) {
  return {radius: 10}
})
//set up the simulation 
var simulation = d3.forceSimulation()
        .nodes(nodes_data)
        .force("collide", d3.forceCollide().radius(d => radius + 1).iterations(3))
        .force('charge', d3.forceManyBody().strength(1))
        //.force('center', d3.forceCenter(width/2, height / 2))
        .force('y', d3.forceY().y(function(d) {
        return height/2;
        }))
        .force('x', d3.forceX().x(function(d) {
        return 0;
        }));
                    
//add tick instructions: 
simulation.on("tick", tickActions );  

//draw circles for the nodes 
var node = svg.append("g")
        .attr("class", "nodes") 
        .selectAll("circle")
        .data(nodes_data)
        .enter()
        .append("circle")
        .attr("r", radius);  

var drag_handler = d3.drag()
	.on("start", drag_start)
	.on("drag", drag_drag)
	.on("end", drag_end);	
	
drag_handler(node)




//drag handler
//d is the node 
function drag_start(d) {
 if (!d3.event.active) simulation.alphaTarget(0.3).restart();
    d.fx = d.x;
    d.fy = d.y;
}

function drag_drag(d) {
  d.fx = d3.event.x;
  d.fy = d3.event.y;
}


function drag_end(d) {
  if (!d3.event.active) simulation.alphaTarget(0);
  d.fx = null;
  d.fy = null;
}
    

function tickActions() {

    //constrains the nodes to be within a box
    
    node.y = 0;
    
    node
    .attr("cx", function(d) { return d.x = Math.max(radius, Math.min(width - radius, d.x)); })
    .attr("cy", function(d) { return d.y = Math.max(radius, Math.min(height - radius, d.y)); });
        
} 

</script>