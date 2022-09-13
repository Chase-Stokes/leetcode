```js

// Solution: 
var fizzBuzz = function(n) {
    let output = [];
    for(i = 1; i <= n; i++) {
        if(i % 15 == 0){
            output.push("FizzBuzz");
        } else if(i % 5 == 0){
            output.push("Buzz");
        } else if(i % 3 == 0){
            output.push("Fizz");
        } else{
            output.push(`${i}`);
        }
    }
    return output;
};

// Solution
var fizzBuzz = function(n) {
    let output = [];
    for(i = 1; i <= n; i++) {
        i % 15 == 0 ? output.push("FizzBuzz") : 
        i % 5 == 0 ? output.push("Buzz") :
        i % 3 == 0 ? output.push("Fizz") : output.push(`${i}`)
    }
    return output;
};



// Example: 
fizzBuzz(15)
0: "1"
1: "2"
2: "Fizz"
3: "4"
4: "Buzz"
5: "Fizz"
6: "7"
7: "8"
8: "Fizz"
9: "Buzz"
10: "11"
11: "Fizz"
12: "13"
13: "14"
14: "FizzBuzz"


```


Posting a coding challenge a day until I get a job.

Day 1

Starting with one that everyone knows FizzBuzz! Let me know if you can think of any ways I can improve my solutions.

Given an integer n, return a string array answer (1-indexed) where:
answer[i] == "FizzBuzz" if i is divisible by 3 and 5.
answer[i] == "Fizz" if i is divisible by 3.
answer[i] == "Buzz" if i is divisible by 5.
answer[i] == i (as a string) if none of the above conditions are true.

#coding #leetcode #javascript #softwarengineering