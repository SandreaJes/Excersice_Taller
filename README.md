# Excersice-Taller
## First-Challenge
 > Given an array of positive integers representing the values of coins in your possession, write a function that returns the minimum amount of change (the minimum sum of money) that you CANNOT create. The given coins can have
  any positive integer value and aren't necessarily unique (i.e., you can have multiple coins of the same value).
  <h3>
  Sample
</h3>
<ol>
  <li>[5, 7, 1, 1, 2, 3, 22] -> 20</li>
  <li>[1, 1, 1, 1, 1] -> 6</li>
  <li>[1, 5, 1, 1, 1, 10, 15, 20, 100] -> 55</li>
  <li>[1, 5] -> 2</li>
  ## Solution
  
function nonContructibleChange(acc: number, elem: number,i,originaArray) {
     
    if(elem>acc+1){
      return acc +1
    }else{
      if((originaArray.length-1)==i){
        return (acc +elem )+1;
      } else{
       // console.log("just acc "+acc+ " in "+i)
        return (acc+elem) ;
      }
    } 
  }
 
const coin = [1,1,1,1];

let minAmount=  coin.sort((x,y)=> x-y).reduce(nonContructibleChange)
  console.log("output is " + minAmount)
  
  ## Second-Challenge
  > Write a function that takes in a non-empty array of integers that are sorted in ascending order and returns a new array of the same length with the squares of the original integers also sorted in ascending order.
  <h3>
  Sample
</h3>

<ol>
  <li>[1, 2, 3, 5, 6, 8, 9] -> [1, 4, 9, 25, 36, 64, 81]</li>
  <li>[-2, -1] -> [1, 4]</li>
  <li>[-10, -5, 0, 5, 10] -> [0, 25, 25, 100, 100]</li>

 ## Solution
 const  arr=  [1, 2, 3, 5, 6, 8, 9] 
  let output = arr.map(x => x * x).sort((x,y)=> x-y)
console.log(" the output is Squared "+output)
