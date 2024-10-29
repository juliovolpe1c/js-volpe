#  let cor;
let X; // horizontal
let Y; // vertical
function setup() {
  createCanvas(800, 500); // width x height
  background(color(0,0,90));
  cor = color(random(0,255), random(0,255), random(0,255));
  X = [0,0,0];
  Y = [random(height), random(height), random(height)];
}
// X = 0,0,0  
// Y = 300, 150 , 150


function draw() {
  
     fill(cor);
  
    //console.log (circuloX.length)
  
  for (let contador in X) {
     // console.log (contador)
  circle(X[contador], Y[contador], 50);  
  X[contador] += random (0,3);
  Y[contador] += random (-3,3);
    
    if (X[contador] >= width){
      X[contador] = 0;
     Y[contador] = random(height);
    }
   
  }
 
  

   if (mouseIsPressed){
    cor = color(random(0,255), random(0,255), random(0,255), random(0,100));
  }
    
}
