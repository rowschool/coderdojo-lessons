# Making Decisions: if-then-else

When we are faced with a simple decision, how do we know which choice to make? Let's say that your family has all of its toothbrushes in the same cup in the bathroom. How do you know which is yours? Do you have the kid-sized toothbrush with the red handle or the one with the Spiderman handle?

When I was a kid and my mom yelled at me, "Eric, get in here." I knew that I had about 60 seconds to get to her; however, if she yelled, "Eric Aloysius, get in here right now," I knew, since she used my fake middle name, that I was in deep trouble and I had roughly 1.5 seconds to appear before her. In my head, I thought, "Given that mom yells my name. If she uses my middle name, I had better drop whatever I'm doing and run to her. Else, I can gently stop whatever I'm doing and quickly walk to her." So, when Mom yelled my name as "Eric Aloysius," did I walk to her or did I run to her?

In code, this might look like:

```javascript
var name;

if (name === "Eric Aloysius") {
  me.dropEverything();
  me.runToMom();
} else {
  me.saveGameOrBookmarkBook();
  me.walkToMom();
}
```

You might notice in the code above, that what happens after I'm called depends on the truth of the name including my middle name or not. This kind of truth is called a "boolean." A boolean value is either true or false (also, yes or no). If-statements, such as the one above, rely on booleans. Let's look at another boolean.

Have you ever made a deal with your parents that if you get a certain grade or score on a test, you can celebrate by doing something special like going out for ice cream or pizza? Let's say that you were required to get a 90% or better on your test in order to celebrate. In this case, the boolean value is "score >= 90." Your score is either greater-than-or-equal-to 90, or it isn't.

```javascript
var score;

if (score >= 90) {
  me.celebrate();
} else {
  me.scrubFloor();
}
```

If I were going to scrub the floor no matter what my score, my code might look a little different:

```javascript
if (score >= 90) {
  me.celebrate();
}

me.scrubFloor();
```

You can also use several if-statements together:

```javascript
var score;

if (score === 100) {
  me.say("WOO!");
} else if (score >= 90) {
  me.say("Woo!");
} else if (score >= 80) {
  me.say("Woo.");
} else if (score >= 70) {
  me.say("ugh");
} else if (score >= 60) {
  me.say("eep!");
} else {
  me.say("Nononononononono");
}
```

You can also check against several booleans (truths) together:

```javascript
var score;
var subject;

if (score < 60 && subject === "spelling") {
  me.askTeacher("Do you offer test retakes?");
}
```

As you can see from these examples, there are several ways to use if-statements to make decisions and move your code along.

## Example Projects

* Scratch: [Number Guesser](https://scratch.mit.edu/projects/197671514/)
* Scratch: Harmony M. [Good or Bad](https://scratch.mit.edu/projects/203315796/)
* Scratch: Tony M. [Shark Bite](https://scratch.mit.edu/projects/197719344/)

## Project Ideas

* Ask the player for a favorite sport, if the sport is played professionally here, reply back with "Go, (name of team)!"
* Get the current temperature, if it's colder than 60 F, show appropriate clothes for the temperature.
