
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
        Shorthand-circuit evaluation
            You can use a variable and the || operator together. for a shortened if else statement
                ex. let defaultName = username || 'stranger';
                If username does not exist the variable will be stranger.
        Ternary Operator
            Use to shorten Boolean if/else statements
                ex. long: 
                    let isNightTime = true;
                    if (isNightTime) {
                    console.log('Yes');
                    } else {
                    console.log('No');
                    }
                    short: 
                    isNightTime ? console.log('Yes'): console.log('No');


    
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

