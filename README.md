# Automata
Simple program for automating keyboard presses and mouse moves/clicks written in NodeJS


## Installation
1. Download this respository
2. Enter the main folder
3. Open console
4. Start program using command `npm run start`

## Programs
You can create your own program or download others. To do so, enter `programs` folder
Here you canadd your programs

## Creating your own program
1. Create new file in `programs` folder with JS extension
2. Paste this string in it:
```js
module.exports.start = function(listner, controller) {
	
	listner.on("mousemove", event => {
		console.log(event);
	});
	
	listner.on("keydown", event => {
		console.log(event);
	});
	
	listner.start();
}

module.exports.config = {
	name: 'myfirst'
}
```
3. Start program, and run program named `myfirst`

### Creating your own program - Functions
`listner` is Object for listning for changes. It emits two events: `mmousemove` and `keydown`<br>
`controller` is Object that's job is controlling mouse and keyboard:<br>
`controller.keyTap("f1")` - Taps the F1 key once<br>
`controller.typeString("Hello World!")` - Writes the inputed String<br>
`controller.moveMouse(x, y)` - Moves the mouse to selected X and Y possition<br>
`controller.getMousePos()` - Return current possiotn of the mouse<br>
`controller.getPixelColor(x, y)` - Return color on selected possition<br>
`controller.getScreenSize` - Return size of the screen<br>
`controller.screen.capture` - Return Bitmap of screen<br>
