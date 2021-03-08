# FSE
let myButton, myButton1;
let myInput, myInput1;
let myText, myText1;
let button1, button2, button3,button4;
let cg;
let bg;
let w1,w2,w3;

function setup() {
  createCanvas(400, 400);
  background('pink');
  
  textSize(25);
  text('WELCOME! LET US START!', 40, 100);
  
  myInput = createInput('Type your name');
  myInput.position(20,150);
  
  myButton = createButton('Start');
  myButton.position(300,340);
  myButton.mousePressed(main);
  myButton1 = createButton('submit');
  myInput1 = createInput('Type your age');
  myInput1.position(20,230);
  myButton1.position(200,230);
  myButton1.mousePressed(doSomething);
  
  myText = ' ';
  myText1 = ' ';
}

function doSomething(){
  myText = myInput.value();
  text('Your name is ' + myText, 20,200);
  
  myText1 = myInput1.value();
  text('Your age is ' + myText1, 20, 280)
}

function main(){
  background('pink');
  myButton.remove();
  myButton1.remove();
  myInput.remove();
  myInput1.remove();
  
  textSize(20);
  text('Which game do you want to play?', 35, 45);
  fill(0,102,153,51);

  let col = color(25,23,200,50);
  button1 = createButton("Tracing");
  button1.style('background-color',col);
  button1.position(170,350);
  button1.mousePressed(trace);
  button1.style("font-family", "Comic Sans MS");
  button1.style("font-size", "15px");
  
  button2 = createButton("Write words");
  button2.style('background-color',col);
  button2.position(25,350);
  button2.mousePressed(chooseWord);
  button2.style("font-family", "Comic Sans MS");
  button2.style("font-size", "15px");
  
  
  button3 = createButton("Color pictures");
  button3.position(280,350);
  button3.style('background-color',col);
  button3.mousePressed(cp);
  button3.style("font-family", "Comic Sans MS");
  button3.style("font-size", "15px");
}

function trace(){
  
  background('lightgreen');
  button1.remove();
 
  let button5 = createButton('main menu');
  button5.position(152,350);
  button5.mousePressed(main);
  textSize(20);
  text('TRACING ALONG THE TRACK!', 35, 45);
  color('rgb(0,0,255)');
  
  
  line(30, 20, 150, 150);
  line(150,150,200,50);
  line(200,50,350,300);

  
}


function chooseWord(){
  background('lightblue');
  button2.remove();
  text('Choose your favorite word!', 60, 45);
  w1 = createButton('Hello');
  w1.position(50,150);
  w1.size(70,70);
  w1.mousePressed(hello);
  w2 = createButton('cat');
  w2.position(130,150);
  w2.mousePressed(cat);
  w2.size(70,70);
  w3 = createButton('red');
  w3.position(210,150);
  w3.mousePressed(redword);
  w3.size(70,70);
  
}
function hello(){
  background('white');
  w1.remove();
  w2.remove();
  w3.remove();
}
function cat(){
  background('white');
  w1.remove();
  w2.remove();
  w3.remove();
}
function redword(){
  background('white');
  w1.remove();
  w2.remove();
  w3.remove();
}
function cp(){
  background('white');
  button3.remove();
  w1.remove();
  w2.remove();
  w3.remove();
  
  
  fill(255);
  stroke(0);
  strokeWeight(7);
  ellipse(215,215,225,225);
  
  fill(255)
  beginShape();
  vertex(330,180)
  vertex(250,180)
  vertex(220,95)
  vertex(180,180)
  vertex(100,180)
  vertex(165,235)
  vertex(140,305)
  vertex(215,265)
  vertex(290,305)
  vertex(265,235)
  endShape(CLOSE);
}
