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

Should do half days in K, pre-K and full days the rest of the months.
How do you do a loop here? Jeez.

```js
let subjects = ['Math', 'Science', 'History', 'English', 'Art', 'Physical Education'];

for (let i = 0; i < subjects.length; i++) {
    console.log('I have ' + subjects[i] + ' class today!');
}
```

Here, the exit condition is that it has looped through each subject in the `subjects` array.

```javascript
let subjects = ['Math', 'Science', 'History', 'English', 'Art', 'Physical Education'];
let subjectCount = 0;

for (i = 0; i < subjects.length; i++) {
    subjectCount += 1;

    if (i === 0) {
        console.log(`I am taking ${subjectCount} subjects.`);
    }

    if (i > 0 && i < subjects.length - 1) {
        console.log(`Just kidding! I am taking ${subjectCount} subjects.`);
    }

    if (i === subjects.length - 1) {
        console.log(`Ok. I am definitely taking ${subjectCount} total subjects.`);
    }
}
```

Notice that we can also do something with the properties that are part of that array, like `length`.

You can also write a loop using a special type of array loop called a `forEach`:

```javascript
const weekdays = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday'];

weekdays.forEach(function(day) {
    console.log(day);
});
```

What are some things that you can loop over? I'll start - you can loop over items in a list, like repeating back the list of items you are supposed to get at the store.

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

Don't do this. It'll go on forever.

```javascript
var i = 0;
do {
    console.log(i++);
} while (i > 0);
```

And also you are definitely quite awesome, don't do this either.

```javascript
var i = 0;
do {
    console.log('I am awesome!');
} while (true);
```

So when is a good time to use an infinite loop? Perhaps while you are waiting for user input in a game or waiting for a status to change. In either case, you want to make sure that you have a way to exit the loop.

- `break` exits a loop
- `continue` skips the current step in the loop

```javascript
while (true) {
    if (this.receivedQuitCommandFromUser()) {
        break;
    }

    this.playRelaxingMusic();
}
```

The following function is written as an infinite loop.

```javascript
const printEvenNumbersToMax = function(maximum) {
    if (!maximum) {
        return;
    }

    for (let i = 1;; i++) { // note that we have no exit condition
        if (i % 2 === 1) {
            continue;
        }

        // this is our exit condition
        if (i >= maximum) {
            break;
        }

        console.log(i);
    }
}
```

And the next one is written as a non-infinite loop.

```javascript
const printEvenNumbersToMax = function(maximum) {
    for (var i = 1; i <= maximum; i++) {
        if (i % 2 === 1) {
            continue;
        }

        console.log(i);
    }
}
```

What's the difference between the two `for` loops?

## Example Projects

* Scratch: Eric P. [Loop Through Names](https://scratch.mit.edu/projects/216162307)
* Scratch: Ethan G. [Cup Game](https://scratch.mit.edu/projects/149735896/)
* Scratch: Eric P. [Random Number Generator](https://scratch.mit.edu/projects/219375454)
* Scratch: Eric P. [Summer Plan: Go hiking!](https://scratch.mit.edu/projects/115901669) (forever loops are used for this animation)

## Project Ideas

* Reduce repeated steps to show a character walking across the screen.
* Read names in a list that start with a letter, like "N".
