# udoo-gpio
NodeJS library for manipulating the GPIOs from the UDOO Board

## Installation
		npm install udoo-gpio

## Usage

		var udoo = require('./udooGPIO.js') //Import the module

		var led = 3 //declare led: GPIO pin 40 --> Arduino pin 13

		//Setup our pin
		function setup() {
		    udoo.pinMode(led, "OUTPUT")
		    udoo.digitalWrite(led, "LOW") //make sure the led is off
		}

		//set a variable off that triggers when the delay is done
		var off = function(){
			udoo.digitalWrite(led, "LOW")
		}

		setup() //call function setup
		udoo.digitalWrite(led, "HIGH")//turn on our led
		udoo.delay(3, off) //wait 3 seconds and turn off


## Release History

* 0.1.0 Initial release
