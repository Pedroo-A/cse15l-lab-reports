# Lab Report 3
## Part 1 - Bugs
---
Failure-inducing input for ArrayExamples.java as a JUnit Test: <br>
```
@Test
public void testReversedError() {
 int[] input1 = { 2,3};
assertArrayEquals(new int[]{3, 2}, ArrayExamples.reversed(input1));
 }
```
  Output: 
  ![Failure inducing output](failure-inducing-output.png)
  <br>Input that doesn't induce a failure <br>
  ```
	@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```
Output: <br>
![Sucessful inout](Sucess-input.png)
<br>
<br>
The bug in ArrayExamples.java causing failure-inducing inputs<br>

```
public class ArrayExamples {

  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
<br>
Bug-fixed code:
<br>

```
public class ArrayExamples {

  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      int temp =arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length-1]=temp;
    }
  }
```
>The error in the code is that the original code does not hold the value of the first value of the array. 
> In the second code it is fixed by creating a temporary variable to store the first value of the array so that it won't be deleted.
---
---
## Part 2 - Researching Commands.
---

  
