# Functions

Have you ever found yourself repeating your code over and over in Scratch or in JavaScript? If you find yourself doing this, you can take advantage of "functions" to reuse the same code over and over again. In Scratch, functions are called "my blocks," but everywhere else, they're called "functions" and sometimes "methods."

All functions do something within your code.

Functions can take input and return output. This is like a popcorn popper at the movie theater: you add popcorn kernels and oil, and you get hot popcorn in return.

Other functions are like commands. They don't take any input, but they do something anyway. It's like telling your dog to sit. You don't tell your dog where to sit, how to sit, how long to sit, or when to sit; you just tell your dog to sit. And guess what? Your dog sits. Good dog!

One way to think about functions is that they let you take a bunch of steps and give them a simple name. This is like teaching a robot to speak. You could tell the robot how to speak each time you want the robot to speak, or you can just create a speak function and tell the robot to do it instead.

```javascript
voiceBox.turnOn();
voiceBox.setVolume(30);
voiceBox.say("Hello"); // This is the part that changes
voiceBox.turnOff();
```

```javascript
voiceBox.turnOn();
voiceBox.setVolume(30);
voiceBox.say("I like to play games"); // This is the part that changes
voiceBox.turnOff();
```

The same, but with functions!

```javascript
function speak(phrase) {
    voiceBox.turnOn();
    voiceBox.setVolume(30);
    voiceBox.say(phrase); // This is the part that relies on the input!
    voiceBox.turnOff();
}
 
speak("Hello");
speak("I like to play games");
```

As you can see, you can create the function once and call it multiple times. Notice, also, that you can have functions call functions, too!

You should also expect the same output for the same input in each function.

```javascript
function double(thing) {
    return thing + thing;
}

let bigPrice = double(2); // output: 4
let tau = double(3.14); // output: 6.28
let freeKidsConferenceInKC = double("kc"); // output: "kckc"

// Check this out
function embiggen(thing) {
    return double(double(double(double(double(double(thing))))));
}

let bigNum = embiggen(2); // output: 128
```

Additional information about [Scratch My Blocks](https://en.scratch-wiki.info/wiki/My_Blocks)
Additional information about [JS functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

## Example Projects

* Scratch: Harmony M. & Adam P. [The Busy Life of Business Cat](https://scratch.mit.edu/projects/228342460/)
* Scratch: Tanner R. [Taco Topper 1.0](https://scratch.mit.edu/projects/133896573/)
* Scratch: Eric P. [Froggy vs. Ravenous Flies](https://scratch.mit.edu/projects/24548080/)

## Project Ideas

* Dance choreography, with each move being a function that describes that move
* A demo of how to cook your favorite meal
