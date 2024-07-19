# Classes and Functions

If you've been coming to CoderDojo for a while, you might have found that we take advantage of "functions" to reuse the same code over and over again.

Have you ever found yourself repeating your code over and over in Scratch or in JavaScript? If you find yourself doing this, you can take advantage of "functions" too. In Scratch, functions are called "my blocks," but everywhere else, they're called "functions" and sometimes "methods."

All functions do something within your code.

Functions can take input and return output. This is like a popcorn popper at the movie theater: you add popcorn kernels and oil, and you get hot popcorn in return.

<img src="https://upload.wikimedia.org/wikipedia/commons/9/99/Popcorn_Pumper_1.JPG" alt="A hot-air home popcorn maker" />

Other functions are like commands. They don't take any input, but they do something anyway. It's like telling your dog to sit. You don't tell your dog where to sit, how to sit, how long to sit, or when to sit; you just tell your dog to sit. And guess what? Your dog sits. Good dog!

<img src="https://upload.wikimedia.org/wikipedia/commons/d/d4/Beagle-Shepard_Mixed-breed_dog_-_Sitting.png" alt="A picture of a dauchund-beagle-shepherd mix dog sitting" />

One way to think about functions is that they let you take a bunch of steps and give them a simple name. This is like teaching a robot to speak. You could tell the robot how to speak each time you want the robot to speak, or you can just create a speak function and tell the robot to do it instead.

In the following block of code, we create a `class` called `VoiceBox` that contains a set of functions we want to call.

This `class` is like a blueprint. We can create an **instance** or as many instances of the class as we want. For examples, if we want to have multiple voiceboxes talking with various volumes or voices, we can create multiple instances.

Note: If you're running this at playcode.io/javascript, you will need to press the Play button.

```javascript
class VoiceBox {
    speaker = window.speechSynthesis;

    voice = null;

    volume = 0.5;

    // to determine which voice to use, debug by `console.log`ging:
    // const voices = window.speechSynthesis.getVoices();
    // voices.forEach(voice => {
    //     console.log(`Voice: ${voice.name}, Language: ${voice.lang}`);
    // });
    constructor(voiceIndex = 0) {
        const voices = this.speaker.getVoices();
        this.voice = voices[voiceIndex];
    }

    turnOn = function() {
        console.log('Activating voice box.');
    }

    turnOff = function() {
        console.log('Deactivating voice box.');
    }

    say = function(words) {
        const utterance = new SpeechSynthesisUtterance(words);
        utterance.voice = this.voice;
        this.speaker.speak(utterance);
        console.log(`"${words}"`)
    }

    setVolume(value) {
        this.volume = value;
        console.log(`Volume set to ${value}.`);
    }
}

const voiceBox = new VoiceBox(0);

voiceBox.turnOn();
voiceBox.setVolume(0.3);
voiceBox.say('Hello');
voiceBox.turnOff();
```

Let's try a different voice!

```js
const voiceBox2 = new VoiceBox(1);

voiceBox2.turnOn();
voiceBox2.setVolume(0.3);
voiceBox2.say('Goodbye');
voiceBox2.turnOff();
```

We can also wrap our `function` calls within a `function` call.

```javascript
function speak(phrase) {
    voiceBox.turnOn();
    voiceBox.say(phrase); // This is the part that relies on the input!
    voiceBox.turnOff();
}
 
speak('Hello');
speak('I like to play games');
```

As you can see, you can create the function once and call it multiple times. Notice, also, that you can have functions call functions, too!

The nice thing about functions is that you can expect the same output for the same input in each `function`.

```javascript
function double(value) {
    if (typeof value === 'number') {
        return value + value;
    }

    if (typeof value === 'string') {
        return `${value}${value}`;
    }
}

const oneLessThanPar = double(2);
console.log(oneLessThanPar);
const tau = double(3.14);
console.log(tau);
const greatMovie = double('CO');
console.log(greatMovie);

// Check this out
function embiggen(thing) {
    return double(double(double(double(double(double(thing))))));
}

const bigNum = embiggen(2);
console.log(bigNum);
```

Additional information about [Scratch My Blocks](https://en.scratch-wiki.info/wiki/My_Blocks)
Additional information about [JS functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

## Example Projects

* Scratch: Tanner R. [Taco Topper 1.0](https://scratch.mit.edu/projects/133896573/)
* Scratch: Eric P. [Froggy vs. Ravenous Flies](https://scratch.mit.edu/projects/24548080/)

## Project Ideas

* Dance choreography, with each move being a function that describes that move
* A demo of how to cook your favorite meal
