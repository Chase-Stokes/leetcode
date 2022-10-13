Given an array of positive integers representing the values of coins in your posession, write a function that returns the minimum amount of change that you cannot create. The given coins can have any positive integer value and aren't nevessarily unique.

Input: [5, 7, 1, 1, 2, 3, 22]
Output = 20

Hint 1:
One approach to sove this is to attempt to create every single amount of change starting at one, and going up until you eventually cant create an amount. AKA Brute Forcing -- There is a better way.

Hint 2:
Start by sorting the input array. Since you're trying to find the minimun amount of change that you can't create, it makes sense to consider the smallest coins first.

Hint 3:
To understand the trick to this problem, consider the following example: coins=[1,2,4]. With this set of coins we can create 1, 2, 3, 4, 5, 6, 7 cents worth of change. Now, if we were to add a coin of value 9 to this set, we would not be able to create 8 cents. However, if we were to add a coin value 7, we would be able to create 8 cents, and we would also be able to create all values of change from 1 to 15. Why is that the case?

```js


//Solution
function nonConstructibleChange(coins) {
  let sortedCoin = coins.sort((a, b) =>  a - b)
  let count = 0
  for(let i = 0; i < sortedCoin.length; i++) {
    if(sortedCoin[i] <= count + 1){
      count += sortedCoin[i]
    }else {
      return count+=1
    }
  }
}

```