//Code for the "Main animation sequence"
========================================================================================
// Variables 
int x1 = -200; // big hills
int x2 = 200;
int x3 = 600;

int x4 = 400; //cloud

int x5 = -200;
int x6 = 0;
int x7 = 200;
int x8 = 400;
int x9 = 600;
int x10 = 800;

int buggsB = 0;

void setup() { //
  size(800,600);
  noStroke();
} // end setup

void draw() { //
  //sky
  background(108, 185, 242); 
  
  fill(250, 250, 250); //cloud
  ellipse (x4, 150, 100, 100);
  ellipse (x4, 200, 100, 100);
  ellipse (x4-50, 200, 100, 100);
  ellipse (x4+50, 200, 100, 100); 
  
  fill(49, 100, 33); //back hills
  ellipse(x1, 400, 400, 400);
  ellipse(x2, 400, 400, 400);
  ellipse(x3, 400, 400, 400);
  
  fill(118, 170, 136); // small hills
  ellipse (x5, 400, 200, 200);
  ellipse (x6, 400, 200, 200);
  ellipse (x7, 400, 200, 200);
  ellipse (x8, 400, 200, 200);
  ellipse (x9, 400, 200, 200);
  ellipse (x10, 400, 200, 200);
  
  fill(201, 193, 103); //ground
  rect(0, 400, 800, 200);

 pushMatrix();
 translate(buggsB, 220);
  bunny();
popMatrix();
  
  buggsB = buggsB + 5;
  if (buggsB ==1000) buggsB = -200;
  
  //move cloud
  x4 = x4 + 1;
  if (x4 == 1000)  x4 = -200;
  
  //move back hills
  x1 = x1 + 2;
  x2 = x2 + 2;
  x3 = x3 + 2;
  if (x1 >= 1000) {
    x1 = -200;
  }
  if (x2 >= 1000) {
    x2 = -200;
  }
  if (x3 >= 1000) {
    x3 = -200; 
  }
  
  //move foreground mountains
  x5 = x5 + 4;
  x6 = x6 + 4;
  x7 = x7 + 4;
  x8 = x8 + 4;
  x9 = x9 + 4;
  x10 = x10 + 4;
  if (x5 >= 1000) {
    x5 = -200;
  }
  if (x6 >= 1000) {
    x6 = -200;
  }
  if (x7 >= 1000) {
    x7 = -200;
  }
  if (x8 >= 1000) {
    x8 = -200;
  }
  if (x9 >= 1000) {
    x9 = -200;
  }
  if (x10 >= 1000) {
    x10 = -200;
  }
}
void bunny() { 
  fill(255);
  ellipse (100, 100, 50, 100);
  ellipse (200, 100, 50, 100);
  ellipse (150, 200, 200, 200); 
  fill(0);
  ellipse (100, 200, 30, 30);
  ellipse (200, 200, 30, 30);

} // end draw 

---------------------------------------------------------------------------------------------
//An image (using coding) I wanted to replace instead of the bunny 

size (400,400);
background(76, 80, 77);

fill(0);
circle(200, 180, 170);
fill(76, 80, 77);
noStroke();
circle(200, 260, 200);
ellipse(200, 130, 7, 200);

fill(0);
ellipse(110, 220, 80, 160);
ellipse(400-110, 220, 80, 160); 

-----------------------------------------------------------------------------------------------------
