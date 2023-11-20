# Lab Report 3
## Part 1 - Bugs
---
Failure-inducing input for ArrayExamples.java as a JUnit Test: <br>
`public void testReverseInPlaceError() {`<br>
 `int[] input1 = { 3, 4 };`<br>
 `ArrayExamples.reverseInPlace(input1);`<br>
 `assertArrayEquals(new int[]{ 4, 3 }, input1);`<br>
  `}`<br>
  Output: 

