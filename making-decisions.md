# Making Decisions: `if` then `else`

When we are faced with a simple decision, how do we know which choice to make? Let's say that your family has all of its toothbrushes in the same cup in the bathroom. How do you know which is yours? Do you have the kid-sized toothbrush with the red handle or the one with the Spider-Man handle?

When I was a kid on weekends, I loved to play outside. I would turn on the weather channel and wait for the meteorologist to deliver the day's weather report. I knew that I could play outside under certain conditions and I knew I had to wear certain clothes under certain conditions.

If it was below 50 &deg;F, my mom would tell me I needed to wear a coat.
If it was rainy, I would have to wear a rain coat.
And if it was below 50 &deg;F and rainy, I'd stay inside and play video games until the weather got better.

In code, this might look like:

```js
const canIGoOutside = function(temperature, weather) {
    if (temperature >= 50) {
        console.log('Mom says I can go outside.');
    }

    if (weather === 'rainy') {
        console.log('Mom says I need to wear a rain coat.');
    }

    if (temperature < 50 && weather === 'rainy') {
        console.log('I don\'t like this weather. I\'m going to stay inside and play video games.');
    }
}
```

You might notice in the code above that what happens after I look at the weather depends on the truth value of the temperature and weather. This kind of truth in code is called a `boolean`. A boolean value is either `true` or `false` (also known as yes or no). `if` statements, like as the one above, rely on booleans. Let's look at another `boolean`.

Have you ever made a deal with your parents that if you get a certain grade or score on a test, you can celebrate by doing something special like going out for ice cream or pizza? Let's say that you were required to get a 90% or better on your test in order to celebrate. 

In this case, the boolean value is `score >= 90`. Your score is either greater-than-or-equal-to `90`, or it isn't.

```javascript
const decideWhetherToCelebrate = function() {
    const score = arguments[0];

    if (score >= 90) {
        console.log('Score is >=90! Celebrate');
    } else {
        console.log('Score is <90. Scrub the floor.');
    }
}
```

What happens when we get an `85`, `90`, or `95`? Predict, observe, and explain.

```js
decideWhetherToCelebrate(85);

decideWhetherToCelebrate(90);

decideWhetherToCelebrate(95);
```

If I were going to scrub the floor no matter what my score, my code might look a little different:

```javascript
const alwaysScrubTheFloor = function() {
    const score = arguments[0];

    if (score >= 90) {
        console.log('Score is >=90! Celebrate');
    }

    console.log('The floors will be clean!');
}
```

Try `alwaysScrubTheFloor(90)` and maybe some others!

You can also use several `if` statements together:

```javascript
const celebrateAppropriately = function() {
    let score = arguments[0];

    if (score === 100) {
        console.log('WOO!');
    } else if (score >= 90) {
        console.log('Woo!');
    } else if (score >= 80) {
        console.log('Woo.');
    } else if (score >= 70) {
        console.log('Ugh.');
    } else if (score >= 60) {
        console.log('Uh oh!');
    } else {
        console.log('Oh nooo!!!');
    }
}
```

You can also check against several boolean values (`true` or `false`) together:

```javascript
const getSpellingTutoring = function(score, subject) {
    if (score < 60 && subject === 'spelling') {
        console.log('Ask the teacher: Do you offer test retakes?');
    }
}
```

As you can see from these examples, there are several ways to use `if` statements to make decisions and move your code along.

## Example Projects

* Scratch: Eric P. [Number Guesser](https://scratch.mit.edu/projects/197671514/)
* Scratch: Harmony M. [Good or Bad](https://scratch.mit.edu/projects/203315796/)
* Scratch: Tony M. [Shark Bite](https://scratch.mit.edu/projects/197719344/)

## Project Ideas

* Ask the player for a favorite sport. If the sport is played professionally here, reply back with "Go, (name of team)!"
* Get the current temperature. If it's colder than 60 &deg;F, show appropriate clothes for the temperature.
