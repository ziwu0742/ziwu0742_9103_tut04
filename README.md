# ziwu0742_week8Quiz

1. # Part 1 Imaging Technique Inspiration
## Piet Mondrian’s Broadway Boogie Woogie 
![Broadway Boogie Woogie](readmeimages/Piet_MondrianBroadway_Boogie_Woogie.jpeg)

Mondrian's artwork offering a framework for balancing structure and spontaneity. The painting’s grid of bold lines and primary colors conveys a sense of order, while the rhythm and repetition evoke **dynamic movement**, akin to the energy of a city or a fast-paced environment. 

[Fading Grid](https://happycoding.io/tutorials/p5js/arrays/fading-grid)
For my creative coding main project, I can incorporate this duality: using a structured layout (such as a grid system) to guide users, while also introducing playful elements, like color or movement, to keep the experience engaging and lively. This approach would express __the beauty of reason__ without sacrificing creativity. 


2. # Part 2 Coding Technique Exploration
## p5.js function draw 
To implement the visual style of Mondrian’s Broadway Boogie Woogie, I can use p5.js, its simple drawing functions to create the geometric shapes and vibrant colors characteristic of his work. p5.js allows for easy manipulation of rectangles and colors, making it an excellent choice for replicating the rhythmic grid of the painting. My artwork can include multiple rectangles with varying sizes, colors, and random placements, as well as a grid-like structure to mimic the dynamic feel of the original artwork. 

> These are some example code created by ChatGPT. 

```
function setup() {
  createCanvas(600, 600);
  noLoop();
}

function draw() {
  background(255);

  // Set up an array of colors
  let colors = [
    color(255, 0, 0),  // Red
    color(0, 0, 255),  // Blue
    color(255, 255, 0), // Yellow
    color(0, 0, 0)     // Black
  ];

  // Draw grid lines
  stroke(0);
  strokeWeight(5);
  for (let x = 0; x <= width; x += 50) {
    line(x, 0, x, height);
  }
  for (let y = 0; y <= height; y += 50) {
    line(0, y, width, y);
  }

  // Draw random rectangles
  for (let i = 0; i < 15; i++) {
    let x = floor(random(0, 12)) * 50;  // Snap to grid
    let y = floor(random(0, 12)) * 50;  // Snap to grid
    let w = floor(random(1, 3)) * 50;    // Width
    let h = floor(random(1, 3)) * 50;    // Height

    fill(random(colors));
    rect(x, y, w, h);
  }

  // Add black lines
  stroke(0);
  strokeWeight(10);
  line(150, 150, 150, 300); // Vertical line
  line(50, 300, 300, 300);  // Horizontal line
}

```