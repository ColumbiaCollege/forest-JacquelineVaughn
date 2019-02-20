//Forrest Project

//variable declarations
PImage t;
final color BLU1=color(138,177,255);
final color BLU2=color(255,255,255);
int dw=2;
int dh=2;

//class declaration
class Tree{
  float x=0;
  float y=100;
  float speed=10;
  Tree(){
    x=random(width);
    y=height/2;
    speed=10;
  }
  void move(){
    x=x+speed;
    if(x>width){
      x=0;
      y=height/2;;
    }
  }
  void display(){
    imageMode(CENTER);
    image(t,x,y,500,500);
  }
}
  Tree[]trees=new Tree[20];
  void setup(){
    //basicc setup
    frameRate(5);
    size(1000,700);
    t=loadImage("tree.png");
    //constructor
    for(int i=0;i<trees.length;i++){
      trees[i]=new Tree();
    }
  }
  
  void draw(){
    //gradient sky
    noStroke();
  for(int x=0;x<width;x+=dw){
    for(int y=0;y<height;y+=dh){
      int loc=x+y*width;
      float ratio=float(loc)/(width*height);
      color c=lerpColor(BLU1,BLU2,ratio);
      fill(c);
      rect(x,y,dw,dh);
    }}
    //tree drawing
    for(int i=0;i<trees.length;i++){
      trees[i].display();
      trees[i].move();
  }
  //ground
  fill(#5C2200);
  rect(0,550,1000,150);
  }
