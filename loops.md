# Loops and Repeating Things

## Introduction to Loops

Loops let you repeat something over and over again. For example:

### Loop example 1

2021 had 12 months: January, February, March, April, May, June, July, August, September, October, November, December

2022 had 12 months: January, February, March, April, May, June, July, August, September, October, November, December

2023 had 12 months: January, February, March, April, May, June, July, August, September, October, November, December

2024 had 12 months: January, February, March, April, ...

Can we just automatically print which months are next using `console.log`?

```js
const months = [
    'January', 'February', 'March', 'April', 'May', 'June', 
    'July', 'August', 'September', 'October', 'November', 'December'
];

const printTheMonths = function(startYear, endYear) {
    for (let currentYear = startYear; currentYear <= endYear; currentYear++) {
        console.log(`${currentYear} had ${months.length} months: ${months.join(', ')}`);
    }
}
```

### Loop example 2

Let's say you spin around and count each spin until you are dizzy. How many times could you spin around?

## Loops in Code

You might notice that we can list the months for every year from `0` to `Infinity`, and these loops could just go on forever. However, we have a conditional for when we can exit the loop - the `startYear` and `endYear`.

Likewise, after spinning around so many times, you're bound to get dizzy and stop.

Most of the time, you want to have an "exit condition" to ensure that you don't have an endless loop in your program.

In JavaScript, the school year could be written as:

// TODO NEIL:
// START IN SEPTEMBER
// END IN MAY
// PAUSE IN JUNE, JULY, AUGUST

```javascript
const months = [
    'January', 'February', 'March', 'April', 'May', 'June', 
    'July', 'August', 'September', 'October', 'November', 'December'
];

const shouldIGoToSchool = function() {

}
// for (i = 0; i < 40; i++) {
//     console.log("Let's go to school this week!");
// }
// Let's go to school this week!
// Let's go to school this week!
// Let's go to school this week!
// Let's go to school this week!
// Let's go to school this week!
// ...
```

Here, the exit condition is that it has looped 12 times. It cannot loop 13 times - unless you go to Kindergarten and/or Pre-K.

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
* Scratch: Ethan G. [Cup Game](https://scratch.mit.edu/projects/149735896/)
* Scratch: [Random Number Generator](https://scratch.mit.edu/projects/219375454)
* Scratch: [Summer Plan: Go hiking!](https://scratch.mit.edu/projects/115901669) -- forever-loops used for animation

## Project Ideas

* Reduce repeated steps to show a character walking across the screen
* Read names in a list that start with the letter "R"
