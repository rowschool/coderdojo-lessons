# Loops and Repeating Things

## Introduction to Loops

Loops let you repeat something over and over again. For example:

### Loop example 1

2015 had 12 months: January, February, March, April, May, June, July, August, September, October, November, December

2016 had 12 months: January, February, March, April, May, June, July, August, September, October, November, December

2017 had 12 months: January, February, March, April, May, June, July, August, September, October, November, December

2018 had 4 months: January, February, March, April, … which months are next?

### Loop example 2

Spin around and count each spin until you are dizzy. How many times could you spin around?

## Loops in Code

Your day could be condensed to “Wake up, do stuff, go to bed.”

```javascript
while (alive) {
    me.wakeUp();
    me.doStuff();
    me.goToBed();
}
```

In Scratch, this could look like:

```javascript
// Scratch
(repeat until (not alive)
    (wakeUp)
    (doStuff)
    (goToBed)
)
```

You’ll notice that even though these loops appear to go on forever, they have a conditional for when they can exit the loop. You want to have an “exit condition” to ensure that you don’t have an endless loop in your program.

In JavaScript, the school year could be written as:

```javascript
for (i = 0; i < 40; i++) {
    console.log("Let's go to school this week!");
}
// Let's go to school this week!
// Let's go to school this week!
// Let's go to school this week!
// Let's go to school this week!
// Let's go to school this week!
// ...
```

Here, the exit condition is that it has looped 40 times. It cannot loop 41 times.

You can also do something with the variables that are part of that loop.

```javascript
var weekdays = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];

for (i = 0; i < weekdays.length; i++ ) {
    console.log(weekdays[i]);
}

// Sunday
// Monday
// Tuesday
// Wednesday
// Thursday
// Friday
// Saturday
// Sunday
```

This could be rewritten using a special type of array loop called a `foreach`:

```javascript
weekdays.forEach(function(day) {
    console.log(day);
});
```

What are some things that you can loop over? You can loop over items in a list, like repeating back the list of items you are supposed to get at the store.

You can also use a loop to repeat an action. For instance, what if I want to have a character walk across the screen? I could say:

```javascript
// Scratch
(move(10))
(useNextCostume)
(wait(1))

(move(10))
(useNextCostume)
(wait(1))

(move(10))
(useNextCostume)
(wait(1))

(move(10))
(useNextCostume)
(wait(1))

(move(10))
(useNextCostume)
(wait(1))
```

Or, I could put those actions in a loop:

```javascript
// Scratch
(repeat(5)
    (move(10))
    (useNextCostume)
    (wait(1))
)
```

## Infinite Loops: good and bad

There's a special kind of loop called an "Infinite Loop" (in Scratch: "Forever Loop"). This is a loop that is easy to create, usually accidentally, and difficult to get out of.

```javascript
// Don't do this
var i = 0;
do {
    console.log(i++);
} while (i > 0);
```

```javascript
// Don't do this, either
var i = 0;
do {
    console.log('I am awesome!');
} while (true);
```

So when is a good time to use an infinite loop? Perhaps while you are waiting for user input in a game or waiting for a status to change. In either case, you want to make sure that you have a way to exit the loop.

- *break:* - this exits a loop
- *continue:* - this skips the current step in the loop

```javascript
while (true) {
    if (this.receivedQuitCommandFromUser()) {
        break;
    }

    this.playRelaxingMusic();
}
```

```javascript
// Written as an infinite loop
printOddNumbersTo: function(topNumber) {
    for (var i = 1;; i++) {
        if (i % 2 === 1) {
            continue;
        }

        // guard statement to get us out of the infinite-loop
        if (i >= topNumber) {
            break;
        }

        console.log(i);
    }
}
```

```javascript
// Written as a non-infinite loop
printOddNumbersTo: function(topNumber) {
    for (var i = 1; i <= topNumber; i++) {
        if (i % 2 === 1) {
            continue;
        }

        console.log(i);
    }
}
```

## Example Projects

* Scratch: [Loop Through Names](https://scratch.mit.edu/projects/216162307)
  <iframe src="https://scratch.mit.edu/projects/embed/216162307/?autostart=false" width="485" height="402" frameborder="0" allowfullscreen="allowfullscreen"></iframe>
* Scratch: Ethan G. [Cup Game](https://scratch.mit.edu/projects/149735896/)
  <iframe src="https://scratch.mit.edu/projects/embed/149735896/?autostart=false" width="485" height="402" frameborder="0" allowfullscreen="allowfullscreen"></iframe>
* Scratch: [Random Number Generator](https://scratch.mit.edu/projects/219375454)
  <iframe src="https://scratch.mit.edu/projects/embed/219375454/?autostart=false" width="485" height="402" frameborder="0" allowfullscreen="allowfullscreen"></iframe>
* Scratch: [Summer Plan: Go hiking!](https://scratch.mit.edu/projects/115901669) -- forever-loops used for animation
  <iframe src="https://scratch.mit.edu/projects/embed/115901669/?autostart=false" width="485" height="402" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

## Project Ideas

* Reduce repeated steps to show a character walking across the screen
* Read names in a list that start with the letter "R"
