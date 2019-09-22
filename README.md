# if-else-game
Instructions for creation of the if-else-game

## 101 ~ The "if" statement
read: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else#Syntax

## 102 ~ Confirm with if demo
Run the following code ( [howto](https://www.quora.com/How-do-I-run-JavaScript-code) )
```javascript
var answer = confirm("Do you confirm?");
if (answer) {
  alert("You do! :D");
} else {
  alert("You don't :(");
}
```

## 103 ~ Confirm quiz game
Now we want to create a game where we can test the users knowledge of different if statement conditions and different operators. For this we need the following demo array:
```javascript
var conditions = [
  'true',
  'false',
  '!true',
  '!false',
  '!!true',
  'true === true',
  'true == 1',
  'true === 1',
  'false == 0',
  'true != false',
  'true !== false',
  'true != 1',
  'true !== 1',
  '1 > 0',
  '0 > 1',
  '9001 > 9000',
  'true > 0',
  'false > true',
  'true || false',
  'false || true',
  'false || false',
  'true && true',
  'false && false',
  'true && false',
  'false && true'
];
```
Now we want to to ask the user each condition and following this we want to evaluate the actual answer to be correct or not.

You should use the following javascript functions:
1. `confirm` [what?](https://developer.mozilla.org/en-US/docs/Web/API/Window/confirm)
1. `some` [for how many?](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
1. `if` [read again](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)
1. `eval` [Evaluate?](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval)
1. Keep the following javascript examples in mind ( [you can run them](https://www.quora.com/How-do-I-run-JavaScript-code) ):
  1. game logic demo:
```javascript
var gameOver = false;
var evaluation = 'false';

var answer = confirm(`Does\n"${evaluation}"\nevaluate to true?`);
if(answer === eval(evaluation)) {
  alert("Nice!");
} else {
  alert("Nope..");
  gameOver = true;
}

if(gameOver) {
  alert("You died..");
} else {
  alert("You win!!");
}
```
  1. foreach demo:
```javascript
var countToSschfiftyFive = [ //https://www.youtube.com/watch?v=-XccUMOQ978
  'Shwam.',
  'Doo.',
  'Two and heif.',
  'Scheven.',
  'Schfourteenteen.',
  'Schwenty one.',
  'Twenty seven heif.',
  'Twenty seven, thirty seven!',
  "Schfifty Five",
];
alert("Let me tell you how to count to Schfifty Five");
countToSschfiftyFive.some((number, index) => {
  if(index === countToSschfiftyFive.length - 1) {
    alert("What you say?");
  }
  alert(number);
  return false; // we just want to loop it all, so it's always false
});
alert("That's how we count to Schfifty Five");
```

