# Chapter 06 - Return values: getting data from functions


### Returning a value from a function
[jsbin: Listing 6.01](http://jsbin.com/yucate/edit?js,console)
```javascript
/* Adventures in JavaScript
 * Listing 6.01
 * Returning a value from a function
 */

var getMessage;
var response;

getMessage = function () {
    return "I’m going on an adventure!";
};

response = getMessage();

console.log(response);



/* Further Adventures
 *
 * 1) Write a getMyMessage function
 *    that returns a message of
 *    your choosing.
 *
 * 2) Write a getLength function
 *    that returns the length of
 *    a string passed in as an argument.
 *    e.g. it should report
 *    "There and back again" has length 20
 *
 */
```


### Using an argument to determine the return value
[jsbin: Listing 6.02](http://jsbin.com/nijijo/edit?js,console)
```javascript
/* Adventures in JavaScript
 * Listing 6.02
 * Using an argument to determine the return value
 */

var getHelloTo;
var fullMessage;

getHelloTo = function (name) {
    return "Hello to " + name;
};

fullMessage = getHelloTo("Kandra");

console.log(fullMessage);



/* Further Adventures
 *
 * 1) Change the definition of getHelloTo
 *    to accept two parameters, name1 and name2.
 *
 * 2) Make the function return a string of
 *    the form "Hello to Kandra and Dax"
 *
 */
```


### Using the return value as an argument
[jsbin: Listing 6.03](http://jsbin.com/yapic/edit?js,console)
```javascript
/* Adventures in JavaScript
 * Listing 6.03
 * Using the return value as an argument
 */

var getHelloTo;

getHelloTo = function (name) {
    return "Hello to " + name;
};

console.log(getHelloTo("Kandra"));
console.log(getHelloTo("Dax"));



/* Further Adventures
 *
 * The JavaScript replace function will
 * replace one string with another.
 * e.g. "Hello Bob".replace("Bob", "Babs");
 * returns the string "Hello Babs"
 *
 * 1) Declare a variable called template
 *    in the function body of getHelloTo.
 *    i.e. var template;
 *
 * 2) Assign it the value "Hello to {{name}}"
 *
 * 3) Replace the {{name}} placeholder
 *    with the value passed in as name. i.e.
 *    template = template.replace("{{name}}", name);
 *
 * 4) Return template from the function.
 *    i.e. return template;
 *
 * 5) Run the function.
 *    Does it still work?
 *
 */
```


### Returning the sum of two numbers
[jsbin: Listing 6.04](http://jsbin.com/haqapu/edit?js,console)
```javascript
/* Adventures in JavaScript
 * Listing 6.04
 * Returning the sum of two numbers
 */

var sum;

sum = function (number1, number2) {
	var total = number1 + number2;

	return total;
};

var result = sum(10, 35);

console.log(result);



/* Further Adventures
 *
 * 1) Find and display the sum of
 *    a different pair of numbers
 *
 * 2) Change the call to console.log so that
 *    the display on the console reads:
 *    'The sum of 10 and 35 is 45'
 *    using the sum function to generate the answer.
 *
 * 3) Can you use the sum function as it is
 *    to add more than two numbers?
 *    Hint: You can nest calls to sum.
 *
 * 4) Create a function to return the sum of
 *    three numbers given as arguments.
 *
 */
```


### A function with three arguments
[jsbin: Listing 6.05](http://jsbin.com/jedigi/edit?js,console)
```javascript
/* Adventures in JavaScript
 * Listing 6.05
 * A function with three arguments
 */

var totalCost;

totalCost = function (callOutCharge, costPerHour, numberOfHours) {
	return callOutCharge + costPerHour * numberOfHours;
};

console.log("$" + totalCost(30, 40, 3));



/* Further Adventures
 *
 * 1) What is the cost for 12 hours work?
 *
 * 2) The plumber sometimes issues discount coupons.
 *    Add a fourth parameter to the totalCost
 *    function definition to account for discounts.
 *
 * 3) Update the function to subtract the discount
 *    from the total before returning it.
 *
 * 4) If a customer has a $20 off coupon,
 *    update the call to totalCost
 *    to display the total cost.
 *    It should now be $130 for 3 hours.
 *
 */
```


### Getting a separator line
[jsbin: Listing 6.06](http://jsbin.com/lijufo/edit?js,console)
```javascript
/* Adventures in JavaScript
 * Listing 6.06
 * Getting a separator line
 */

var getLine;

getLine = function (lineLength, character) {
    var line;
    var characterStartIndex;

    line = "****************************************";
    line += "----------------------------------------";
    line += "========================================";
    line += "++++++++++++++++++++++++++++++++++++++++";

    characterStartIndex = line.indexOf(character);

    return line.substr(characterStartIndex, lineLength);
};

console.log(getLine(10, "+"));
console.log(getLine(3, "="));



/* Further Adventures
 *
 * 1) Update the getLine function to include
 *    ~ as a possible separator option. (tilde)
 *
 * This one could be a bit of a challenge!
 *
 * 2) Write a getBox function that accepts
 *    some text and a character to use as
 *    a border. The function should return
 *    the text surrounded by a border made
 *    of the specified character.
 *    e.g. getBox("To Infinity!", "+") should return
 *
 *    ++++++++++++++++
 *    + To Infinity! +
 *    ++++++++++++++++
 *
 *    You can use the getLine function.
 *
 * To add a new line in your string, use \n.
 * All strings have a length property.
 *
 */
```


### Getting a string for a player’s name
[jsbin: Listing 6.07](http://jsbin.com/hijeli/edit?js,console)
```javascript
/* Adventures in JavaScript
 * Listing 6.07
 * Getting a string for a player’s name
 */

var getPlayerName;

getPlayerName = function (playerName) {
    return playerName;
};

console.log(getPlayerName("Kandra"));



/* Further Adventures
 *
 * 1) Update the getPlayerName function
 *    so it adds a prefix and suffix
 *    made up of the = character.
 *    The length of the prefix and suffix
 *    should be the same as the player's name.
 *
 *    getPlayerName("Kiki") should return
 *    ==== Kiki ====
 *
 *    getPlayerName("Mahesha") should return
 *    ======= Mahesha =======
 *
 */
```


### Getting strings for a player’s health and location
[jsbin: Listing 6.08](http://jsbin.com/pemore/edit?js,console)
```javascript
/* Adventures in JavaScript
 * Listing 6.08
 * Getting strings for a player’s health and location
 */

var getPlayerHealth;
var getPlayerPlace;

getPlayerHealth = function (playerName, playerHealth) {
    return playerName + " has health " + playerHealth;
};

getPlayerPlace = function (playerName, playerPlace) {
    return playerName + " is in " + playerPlace;
};

console.log(getPlayerHealth("Kandra", 50));
console.log(getPlayerPlace("Kandra", "The Dungeon of Doom"));



/* Further Adventures
 *
 * 1) Change the two functions so they only
 *    show the first three letters of a
 *    player's name as part of the returned string.
 *    e.g. Kan... health 50
 *    e.g. Kan... in The Dungeon of Doom
 *
 * 2) Further change them so they also
 *    transform the names to upper case.
 *    e.g. KAN... health 50
 *    e.g. KAN... in The Dungeon of Doom
 *
 */
```


### Getting a string for a player’s information
[jsbin: Listing 6.09](http://jsbin.com/javuxe/edit?js,console)
```javascript
/* Adventures in JavaScript
 * Listing 6.09
 * Getting a string for a player’s information
 */

var getPlayerName;
var getPlayerHealth;
var getPlayerPlace;
var getPlayerInfo;
var getLine;

getPlayerName = function (playerName) {
    return playerName;
};

getPlayerHealth = function (playerName, playerHealth) {
    return playerName + " has health " + playerHealth;
};

getPlayerPlace = function (playerName, playerPlace) {
    return playerName + " is in " + playerPlace;
};

getLine = function (lineLength, character) {
    var line;
    var characterStartIndex;

    line = "****************************************";
    line += "----------------------------------------";
    line += "========================================";
    line += "++++++++++++++++++++++++++++++++++++++++";

    characterStartIndex = line.indexOf(character);

    return line.substr(characterStartIndex, lineLength);
};

getPlayerInfo = function (playerName, playerPlace, playerHealth) {
    var playerInfo;

    playerInfo = "\n" + getPlayerName(playerName);
    playerInfo += "\n" + getLine(20, "*");
    playerInfo += "\n" + getPlayerPlace(playerName, playerPlace);
    playerInfo += "\n" + getPlayerHealth(playerName, playerHealth);
    playerInfo += "\n" + getLine(20, "*");
    playerInfo += "\n";

    return playerInfo;
};

console.log(getPlayerInfo("Kandra", "The Dungeon of Doom", 50));



/* Further Adventures
 *
 * There is a JavaScript function to return the
 * smaller of two numbers.
 * e.g. Math.min(3, 8) returns 3
 * e.g. Math.min(45, 40) returns 40
 *
 * There is another function to return the
 * larger of two numbers.
 * e.g. Math.max(3, 8) returns 8
 * e.g. Math.max(45, 40) returns 40
 *
 * In the getLine function, you want the
 * lineLength to be between 0 and 40.
 *
 * 1) In the getLine function, before the return statement,
 *    add these two lines:
 *    lineLength = Math.max(0, lineLength);
 *    lineLength = Math.min(40, lineLength);
 *
 *    They will make sure lineLength is between 0 and 40.
 *
 * 2) Update the getPlayerInfo function so that
 *    the line separators are the same length
 *    as the string returned by getPlayerPlace,
 *    up to a length of 40.
 *    You can declare new variables if required.
 *
 */
```


### Displaying player information using objects
[jsbin: Listing 6.10](http://jsbin.com/puteki/edit?js,console)
```javascript
/* Adventures in JavaScript
 * Listing 6.10
 * Displaying player information using objects
 */

var getPlayerName = function (playerName) {
    return playerName;
};

var getPlayerHealth = function (playerName, playerHealth) {
    return playerName + " has health " + playerHealth;
};

var getPlayerPlace = function (playerName, playerPlace) {
    return playerName + " is in " + playerPlace;
};

var getLine = function (lineLength, character) {
    var line;
    var characterStartIndex;

    line = "****************************************";
    line += "----------------------------------------";
    line += "========================================";
    line += "++++++++++++++++++++++++++++++++++++++++";

    characterStartIndex = line.indexOf(character);

    return line.substr(characterStartIndex, lineLength);
};

var getPlayerInfo = function (playerName, playerPlace, playerHealth) {
    var playerInfo;

    playerInfo = "\n" + getPlayerName(playerName);
    playerInfo += "\n" + getLine(32, "=");
    playerInfo += "\n" + getPlayerPlace(playerName, playerPlace);
    playerInfo += "\n" + getPlayerHealth(playerName, playerHealth);
    playerInfo += "\n" + getLine(32, "=");
    playerInfo += "\n";

    return playerInfo;
};

var player1 = {
    name: "Kandra",
    place: "The Dungeon of Doom",
    health: 50
};

var player2 = {
    name: "Dax",
    place: "The Old Library",
    health: 40
};

console.log(getPlayerInfo(player1.name, player1.place, player1.health));
console.log(getPlayerInfo(player2.name, player2.place, player2.health));



/* Further Adventures
 *
 * 1) Add an items property to both players.
 *    e.g. items: "a rusty key, a piece of cheese"
 *
 * 2) Create a getPlayerItems function to return
 *    a sensible string including the items.
 *
 * 3) Update the getPlayerInfo function to
 *    include a call to getPlayerItems.
 *
 * 4) Change the two calls to getPlayerInfo
 *    so they also pass the items property
 *    as an argument.
 *
 */
```