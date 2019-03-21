# clase2-21-0319
#clima en London

var tiempo;

function preload(){
	//usen la suya
	var key = "92528b295c0baa4fbcb50c8a49e0ffdf";
	var city = "London,UK";
	tiempo = loadJSON ("https://api.openweathermap.org/data/2.5/weather?q=" + city + "&units=metric&APPID=" + key)
}

function setup(){
	createCanvas(400, 400);
	print (tiempo);
	noLoop();
}

function draw(){
	background(200);
	var calor = tiempo.main.temp;
	if (calor < 15){
		fill(255,0,0);
	} else {
		fill(0,0,225);
	}
	textSize(36)
	text(tiempo.main.temp,10,40);
}
