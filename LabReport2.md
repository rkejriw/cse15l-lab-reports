# Lab Report 2

This lab report will consist of three Parts:

1. Part 1 - StringServer
2. Part 2 - One bug from Lab 3
3. Part 3 - Learning from Labs in Week 2 or Week 3

## Part 1

*

## Part 2

* One bug from Lab 3 that I will be addressing in this report is the error in the method **reversed**.
* A failure-inducing input for the buggy program, is writing a test case such as:
```
@Test
public void testReversed1() {
  int[] input1 = {1,2,3};
  assertArrayEquals(new int[]{3,2,1}, ArrayExamples.reversed(input1));
}
```
* An input that doesn’t induce a failure, is writing a test case such as:
```
@Test
public void testReversed() {
  int[] input1 = { };
  assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
}
```
* The symptom, as the output of running these tests is the following:
![Image](Symptomlab3.png)

* The bug, as the before-and-after code change required to fix it is the following:

    **BEFORE :**
```
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = newArray[arr.length - i - 1];
  }
  return arr;
}
```
* The before code is assigning new values to the array arr in the for loop instead of the newArray and is also returning arr back instead of newArray. This causes an error in testReversed1 as the expected output and the actual output do not match.

    **AFTER :**
    
```
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    newArray[arr.length - i - 1] = arr[i];
  }
  return newArray;
}
```
* The after code is now giving the correct output and working because now, the for loop is iterating through the array arr to assign new values to the array newArray. I have also corrected the return value to now be newArray because we want the newArray to give us the reversed values. Thus, the actual and expected output now match and the bug has been removed by these fixes.

## Part 3

