class Walker1 {
  int x;
  int y;
  
  
    Walker1() {
    x = width/2;
    y = height/2;
    }
    void display() {
      stroke(100,200,0);
      ellipse(x,y,10,10);
      fill(100,200,0);
      strokeWeight(1);
      point(x,y);
    }
    void step() {
      int choice = int(random(4));
      if (choice == 0) {
        x = x+10;
      } else if (choice == 1) {
        x = x-10;
      } else if (choice == 2) {
        y = y+10;
      } else {
        y = y-10;
      }
    }
}
class Walker2 {
  int x;
  int y;
  
    Walker2() {
    x = width/2;
    y = height/2;
    }
    void display() {
      stroke(100,0,200);
      ellipse(x,y,10,10);
      fill(100,0,200);
      strokeWeight(5);
      point(x,y);
    }
    void step() {
      int choice = int(random(4));
      if (choice == 0) {
        x = x+10;
      } else if (choice == 1) {
        x = x-10;
      } else if (choice == 2) {
        y = y+10;
      } else {
        y = y-10;
      }
    }
}
Walker1 w1;
Walker2 w2;

void setup() {
  size(1640,960);
  w1 = new Walker1();
  w2 = new Walker2();
  background(255);
}
void draw() {
  w1.step();
  w1.display();
  w2.step();
  w2.display();
}
