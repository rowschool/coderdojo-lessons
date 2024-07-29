# User Input: Text

If you ask almost any mentor in the CoderDojo who they write programs for, they will tell you that they write them for clients - who are just other people. All of these programs rely upon input from those other people in order to be useful.

If you think about the games that you love to play, those games are fun to play because they rely upon some kind of input from you. It could be the press of a button, wiggling a joystick, or typing an answer.

Today, we'll look at how to input text in order to get output from your program.

### Scratch

In Scratch, we have one way of getting user input as text - the 'ask' block:

<img src="images/input-text/ask.png" width="640px" alt="A Scratch 'ask' block" />

This will ask for input and store that input as an answer variable that you can use later.

<img src="images/input-text/answer.png" width="300px" alt="A Scratch 'answer' block" />

If you ask several questions, you will want to store each of those answers in a different variable before asking another question.

<img src="images/input-text/save-answer.png" width="640px" alt="A Scratch 'set variable to' block to set the 'backwardsName' variable to the answer from the text input" />

### JavaScript

In JavaScript, you can get user input by using a `<form>`. A `<form>` can take in text (`<input type="text">`), ask questions where the user has to select either "yes" or "no" (`<input type="radio">`) offer a dropdown list for users to select one or more options (`<select>` with `<option>`s), and others. Each form part should have a unique `id` since that the answer to that part of the form will be tied to the `id`.

For example:

```html
<input type="text" id="place">
<button type="submit" id="submit">Submit</button>
```

In JavaScript, you would then pull information out of that form to be used in your code. You can do that by assigning the data tied to those form part IDs to variables.

```javascript
let place = document.querySelector('#place');
```

You can then show that answer in a string by using a [template literal](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals).

```javascript
`I love ${place.value}. It is such a cool place to visit!`
```

The Mozilla Developer Network has a [great introduction to forms](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms) if you'd like to learn more about creating forms in HTML.

## Example Projects

- Scratch: Eric P. [Your Name Backwards](https://scratch.mit.edu/projects/238779843/)
- Scratch: Yusuf S. [AMERICA](https://scratch.mit.edu/projects/168370618/)

## Project Ideas

- [Mad Libs](https://en.wikipedia.org/wiki/Mad_Libs)
- Calculator
- Flash cards
- Trivia game