

Logical Operators
    if (stopLight === 'green' && pedestrians === 0) {
            console.log('Go!');
        } else {
            console.log('Stop');
        }
    Logical Operators
        &&- And
        ||- Or
        !- Opposite or False 
    Improving If(){} Else{} statements with Operators
        Check to see if a variable exists:
            if (myVariable) -This checks if the variable exists
            This is true because the variable exists and doesn't have a false value. 
                -False values: 0, empty string, null, undefined, or Not a Number
        Shorthand-circuit evaluation:
            You can use a variable and the || operator together. for a shortened if else statement
                ex. let defaultName = username || 'stranger';
                If username does not exist the variable will be stranger.
        Ternary Operator:
            Use to shorten Boolean if/else statements
                ex. long: 
                    let isNightTime = true;
                    if (isNightTime) {
                    console.log('Yes');
                    } else {
                    console.log('No');
                    }
                    short: 
                    isNightTime ? console.log('Yes') : console.log('No');
                ex 2. 
                    walkSignal === 'Walk' ? console.log('You may walk!') : console.log('Do not walk!'); 
            In the example above:
            The condition, isNightTime, is provided before the ?.
            Two expressions follow the ? and are separated by a colon :.
            If the condition evaluates to true, the first expression executes.
            If the condition evaluates to false, the second expression executes.
            Like if...else statements, ternary operators can be used for conditions which evaluate to true or false.

    
    Activities
    1.
        Summary: create a if else statement with a AND statement
            1. Create a variable named mood, set it to 'sleepy'
            2. create a variable named tirednessLevel, set it to '6'
            3. Let's create an if...else statement that checks if mood is 'sleepy' and tirednessLevel is greater than 8.
            4. If both conditions evaluate to true, then console.log() the string 'time to sleep'. Otherwise, we should console.log() 'not bed time yet'.
            5. After you press "Run", play around with the || operator and the ! operator! What happens if you negate the value of the entire statement with ! and switch to || instead of &&?

        Solution: 
            let mood = 'sleepy';
            let tirednessLevel = 6;

            if (mood === 'sleepy' && tirednessLevel > 8) {
            console.log('time to sleep');
            } else {
            console.log('not bed time yet')
            }
    2.
        Summary: Practice Shorthand cicuit evaluation
            1. Simplify
                let defaultName;
                if (username) {
                defaultName = username;
                } else {
                defaultName = 'Stranger';
                }
        Solution
            let defaultName = username || 'Stranger';
    3. 

Else/If Statements
    Introduction: 
        We can add more conditions to our if...else with an else if statement. The else if statement allows for more than two possible outcomes. You can add as many else if statements as you’d like, to make more complex conditionals!
        ex. 
            (stopLight === 'red') {
            console.log('Stop!');
            } else if (stopLight === 'yellow') {
            console.log('Slow down.');
            } else if (stopLight === 'green') {
            console.log('Go!');
            } else {
            console.log('Caution, unknown!');
            }
        The else if statements allow you to have multiple possible outcomes. if/else if/else statements are read from top to bottom, so the first condition that evaluates to true from the top to bottom is the block that gets executed.

        In the example above, since stopLight === 'red' evaluates to false and stopLight === 'yellow' evaluates to true, the code inside the first else if statement is executed. The rest of the conditions are not evaluated. If none of the conditions evaluated to true, then the code in the else statement would have executed.
    
Switch Statements
    Introduction: 
        Problem: we have a series of conditions checking for a value that matches a groceryItem variable. Our code works fine, but imagine if we needed to check 100 different values! Having to write that many else if statements sounds like a pain!

        Solution: A switch statement provides an alternative syntax that is easier to read and write. A switch statement looks like this:
            let groceryItem = 'papaya';

            switch (groceryItem) {
            case 'tomato':
                console.log('Tomatoes are $0.49');
                break;
            case 'lime':
                console.log('Limes are $1.49');
                break;
            case 'papaya':
                console.log('Papayas are $1.29');
                break;
            default:
                console.log('Invalid item');
                break;
            }
        Format: 
            switch (true variable to be compared) {
                case 'variable comparison':
                    action;
                    break;
                case 'variable comparison':
                    action;
                    break;
            }
        Instead of a giant if/else if statement. We just say in the case that the variable is _____ do this.
    Activity: 
        1. Create a magic eight ball that console.logs 8 possible responses.
        2. Use a switch function. 
    Solution: 
        var randomNumber = Math.floor(Math.random() * 8);
        var eightBall = "";
        eightBall = randomNumber;
        switch (eightBall) {
            case 0:
                console.log('It is certain');
                break;
            case 1:
                console.log('1');
                break;
            case 2:
                console.log('2');
                break;
            case 3:
                console.log('3');
                break;
            case 4:
                console.log('4');
                break;
            case 5:
                console.log('5');
                break;
            case 6:
                console.log('6');
                break;
            case 7:
                console.log('7');
                break;
        }
    Activity: 
        Race Day
            Codecademy's annual race is just around the corner! This year, we have a lot of participants. You have been hired to write a program that will register runners for the race and give them instructions on race day.

            As a timeline, registration would look like this: registration-timeline

            Here's how our registration works. There are adult runners (over 18 years of age) and youth runners (under 18 years of age). They can register early or late. Runners are assigned a race number and start time based on their age and registration.

            Race number:

            Early adults receive a race number at or above 1000.
            All others receive a number below 1000.
            Start time:

            Adult registrants run at 9:30 am or 11:00 am.
            Early adults run at 9:30 am.
            Late adults run at 11:00 am.
            Youth registrants run at 12:30 pm (regardless of registration).
    Solution: 
        let raceNumber = Math.floor(Math.random() * 1000);
                <!-- Set runner Parameters, can be any -->
        let runnerEarly = true;
        let runnerAge = 26;
        <!-- Make starting random number -->
        if (runnerEarly === true && runnerAge > 18) {
        raceNumber += 1000;
        } 
        <!-- Run the test to print -->
        if (runnerAge > 18 && runnerEarly === true) {
        console.log("Your race will start at 9:30 am and your race number is " + raceNumber);
        } else if (runnerEarly === false && runnerAge > 18) {
        console.log("Your race will start at 11:00 am and your race number is " + raceNumber);
        } else if (runnerAge<18) {
        console.log("Your race will start at 12:30 pm and your race number is " + raceNumber);
        } else {
        console.log("See registration desk");
        }
        

        
            

Review: 
Review
    An if statement checks a condition and will execute a task if that condition evaluates to true.
    if...else statements make binary decisions and execute different code blocks based on a provided condition.
    We can add more conditions using else if statements.
    Comparison operators, including <, >, <=, >=, ===, and !== can compare two values.
    The logical and operator, &&, or "and", checks if both provided expressions are truthy.
    The logical operator ||, or "or", checks if either provided expression is truthy.
    The bang operator, !, switches the truthiness and falsiness of a value.
    The ternary operator is shorthand to simplify concise if...else statements.
    A switch statement can be used to simplify the process of writing multiple else if statements. The break keyword stops the remaining cases from being checked and executed in a switch statement.
--------------------------------------------------------------------------------
Chapter 2: We Out Here Trying to Function
--------------------------------------------------------------------------------
An Introduction 
    In JavaScript, there are many ways to create a function. One way to create a function is by using a function declaration. Just like how a variable declaration binds a value to a variable name, a function declaration binds a function to a name, or an identifier. Take a look at the anatomy of a function declaration below:
   
    A function declaration consists of:
        The function keyword.
        The name of the function, or its identifier, followed by parentheses.
        A function body, or the block of statements required to perform a specific task, enclosed in the function’s curly brackets, { }.
        A function declaration is a function that is bound to an identifier, or name. In the next exercise we'll go over how to run the code inside the function body.

    We should also be aware of the hoisting feature in JavaScript which allows access to function declarations before they're defined.

    Take a look at example of hoisting:

    console.log(greetWorld()); // Output: Hello, World!

    function greetWorld() {
    console.log('Hello, World!');
    }
    Notice how hoisting allowed greetWorld() to be called before the greetWorld() function was defined! Since hoisting isn't considered good practice, we simply want you to be aware of this feature.

Functions with Parameters and Arguments
    So far, the functions we've created execute a task without an input. However, some functions can take inputs and use the inputs to perform a task. When declaring a function, we can specify its parameters. Parameters allow functions to accept input(s) and perform a task using the input(s). We use parameters as placeholders for information that will be passed to the function when it is called.
Function Expressions
    Function expressions are not named and are often put into const variables.
        ex. const calculateArea = function(width,height) { const area = height * width; return area;}
Function Expressions: Shorthand Arrow Functions
    ES6 introduced arrow function syntax, a shorter way to write functions by using the special "fat arrow" () => notation.

    Arrow functions remove the need to type out the keyword function every time you need to create a function. Instead, you first include the parameters inside the ( ) and then add an arrow => that points to the function body surrounded in { } like this:
        Replace function () {} with () => {}
        ex.
            const rectangleArea = (width, height) => {
            let area = width * height;
            return area
            }
Function Expressions: Shorthand Arrows and Return shorthand
    Shorthand to replace a long writter return function
        ex.
            const sum = (number) =>               const sum = number => number + number;
                const sum = number + number; --->
                return sum;
            }
Scoping: 
    In this lesson, you learned about scope and how it impacts the accessibility of different variables.

    Scope is the idea in programming that some variables are accessible/inaccessible from other parts of the program.
    Blocks are statements that exist within curly braces {}.
    Global scope refers to the context within which variables are accessible to every part of the program.
    Global variables are variables that exist within global scope.
    Block scope refers to the context within which variables that are accessible only within the block they are defined.
    Local variables are variables that exist within block scope.
    Global namespace is the space in our code that contains globally scoped information.
    Scope pollution is when too many variables exist in a namespace or variable names are reused.
    As you continue your coding journey, remember to use best practices when declaring your variables! Scoping your variables tightly will ensure that your code has clean, organized, and modular logic.

Review:
    Give yourself a pat on the back, you just navigated through functions!

    In this lesson, we covered some important concepts about functions:
    * A function is a reusable block of code that groups together a sequence of statements to perform a specific task.
    * A function declaration : Diagram showing the syntax of a function declaration
    * A parameter is a named variable inside a function's block which will be assigned the value of the argument passed in when the function is invoked: JavaScript syntax for declaring a function with parameters
    * To call a function in your code: Diagram showing the syntax of invoking a function
    * ES6 introduces new ways of handling arbitrary parameters through default parameters which allow us to assign a default value to a parameter in case no argument is passed into the function.
    * To return a value from a function, we use a return statement.
    * To define a function using function expressions: defining a function expression
    * To define a function using arrow function notation: 
    * Function definition can be made concise using concise arrow notation: comparing single line and multiline arrow functions
    * It's good to be aware of the differences between function expressions, arrow functions, and function declarations. As you program more in JavaScript, you'll see a wide variety of how these function types are used.



Activities
    1. Why does this return undefined?
        function rectangleArea(width, height) {
        let area = width * height 
        }
        console.log(rectangleArea(5, 7)) // 
    2. Create a function expression that tells you to water the plants if it is Wednesday. Start with a constant variable/
        Solution: 
            const plantNeedsWater = function(day){ 
            if (day === 'Wednesday') {
            return true;
            } else {return false;}
            }
            plantNeedsWater('Tuesday');
            console.log(plantNeedsWater('Tuesday'));


--------------------------------------------------------------------------------
Chapter 3: Looptidy Scoop, Looptidy Whoop Poop
--------------------------------------------------------------------------------

The While Loop
    You’re doing great! We're going to teach you about a different type of loop: the while loop. To start, let's convert a for loop into a while loop:

    // A for loop that prints 1, 2, and 3
    for (let counterOne = 1; counterOne < 4; counterOne++){
    console.log(counterOne);
    }

    // A while loop that prints 1, 2, and 3
    let counterTwo = 1;
    while (counterTwo < 4) {
    console.log(counterTwo);
    counterTwo++;
    }
    Let's break down what's happening with our while loop syntax:

    The counterTwo variable is declared before the loop. We can access it inside our while loop since it's in the global scope.
    We start our loop with the keyword while followed by our stopping condition, or test condition. This will be evaluated before each round of the loop. While the condition evaluates to true, the block will continue to run. Once it evaluates to false the loop will stop.
    Next, we have our loop's code block which prints counterTwo to the console and increments counterTwo.
    What would happen if we didn't increment counterTwo inside our block? If we didn't include this, counterTwo would always have its initial value, 0. That would mean the testing condition counterTwo < 4 would always evaluate to true and our loop would never stop running! This is called an infinite loop and it's something we always want to avoid. Infinite loops can take up all of your computer's processing power potentially freezing your computer.

    So you may be wondering when to use a while loop! The syntax of a for loop is ideal when we know how many times the loop should run, but we don't always know this in advance. Think of eating like a while loop: when you start taking bites, you don't know the exact number you'll need to become full. Rather you'll eat while you're hungry. In situations when we want a loop to execute an undetermined number of times, while loops are the best choice.

Do...While Statements
    Review:
        Great job! In this lesson, we learned how to write cleaner code with loops. You now know:
        Loops perform repetitive actions so we don’t have to code that process manually every time.
        How to write for loops with an iterator variable that increments or decrements
        How to use a for loop to iterate through an array
        A nested for loop is a loop inside another loop
        while loops allow for different types of stopping conditions
        Stopping conditions are crucial for avoiding infinite loops.
        do...while loops run code at least once— only checking the stopping condition after the first execution
        The break keyword allows programs to leave a loop during the execution of its block

The .map() Method
    The second iterator we're going to cover is .map(). When .map() is called on an array, it takes an argument of a callback function and returns a new array! Take a look at an example of calling .map():

        const numbers = [1, 2, 3, 4, 5]; 

        const bigNumbers = numbers.map(number => {
        return number * 10;
        });
        .map() works in a similar manner to .forEach()— the major difference is that .map() returns a new array.

    In the example above:

    numbers is an array of numbers.
    bigNumbers will store the return value of calling .map() on numbers.
    numbers.map will iterate through each element in the numbers array and pass the element into the callback function.
    return number * 10 is the code we wish to execute upon each element in the array. This will save each value from the numbers array, multiplied by 10, to a new array.
    If we take a look at numbers and bigNumbers:

    console.log(numbers); // Output: [1, 2, 3, 4, 5]
    console.log(bigNumbers); // Output: [10, 20, 30, 40, 50]
    Notice that the elements in numbers were not altered and bigNumbers is a new array.
--------------------------------------------------------------------------------
Chapter 4: Iterators
--------------------------------------------------------------------------------
The .findIndex() Method
    We sometimes want to find the location of an element in an array. That's where the .findIndex() method comes in! Calling .findIndex() on an array will return the index of the first element that evaluates to true in the callback function.

        const jumbledNums = [123, 25, 78, 5, 9]; 

        const lessThanTen = jumbledNums.findIndex(num => {
        return num < 10;
        });
    jumbledNums is an array that contains elements that are numbers.
    const lessThanTen = declares a new variable that stores the returned index number from invoking .findIndex().
    The callback function is an arrow function has a single parameter, num. Each element in the jumbledNums array will be passed to this function as an argument.
    num < 10; is the condition that elements are checked against. .findIndex() will return the index of the first element which evaluates to true for that condition.
    Let's take a look at what lessThanTen evaluates to:

        console.log(lessThanTen); // Output: 3
        If we check what element has index of 3:

        console.log(jumbledNums[3]); // Output: 5
        Great, the element in index 3 is the number 5. This makes sense since 5 is the first element that is less than 10.

        If there isn't a single element in the array that satisfies the condition in the callback, then .findIndex() will return -1.

        const greaterThan1000 = jumbledNums.findIndex(num => {
        return num > 1000;
        });

        console.log(greaterThan1000); // Output: -1

The .reduce() Method
    Use the .reduce method to add an array together. It takes a  call back function that takes 2 arguments. The .reduce will hit that function each time for every section of the array.
        array.reduce(function(accumulatorValue,arrayValue), initialAcumulatorValue);
The .filter() Method
    Use the filter method by putting a call back function that takes the argument of the element in the array. For example a number or a string. Then tell the function to return the arguments with your paramenters.
        ex.
            const words = ['unique', 'uncanny', 'pique', 'oxymoron', 'guise'];
            const interestingWords = words.filter(
                function (word){ 
                return word.length > 5;
            }
            );
            Result: [ 'unique', 'uncanny', 'oxymoron' ]
The .every() Method
    Use the every method to test if all elements in an array pass the parameters
console.log(interestingWords);

Loop Cheat Sheet
    var array = ['a','b','c','d']

    for (let item of array) { // Of - Loops through items of array
    console.log("Let Of " + item)
    }

    for (let index in array) { // In - Loops through indices in array
    console.log("Let In " + index)
    }

    for (var i=0; i < array.length; i++) {
    console.log("Item " + array[i]) // array[i] - returns items of array
    }

    for (var i=0; i < array.length; i++) {
    console.log("Index " + i) // i - returns indices in array
    }