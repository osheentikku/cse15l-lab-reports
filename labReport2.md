# Lab Report 2

## Part 1
Here is the code for StringServer:

![code](https://user-images.githubusercontent.com/32721916/215294628-08c9ce88-df4f-4099-a124-be530779f6e2.png)

1. When adding the word "Hello":

![addHello](https://user-images.githubusercontent.com/32721916/215285381-85b0a984-1a18-4bba-8338-42a858e76319.png)
* Calls: ```handleRequest```
* Relevant Arguments: ```URI url```
* Values of Relevant fields: ```parameters = [s, Hello]; s = "Hello \n"```
* Changed Values: From this specific request, a new String array called parameters is created using the query and the value s is changed so that it includes the added string.

2. When adding the word "Goodbye":

![addGoodbye](https://user-images.githubusercontent.com/32721916/215285963-ff1e2b12-25bd-4aaa-8c4d-ee41f7887238.png)
* Calls: ```handleRequest```
* Relevant Arguments: ```URI url```
* Values of Relevant fields: ```parameters = [s, Goodbye]; s = "Hello \n Goodbye \n"```
* Changed Values: From this specific request, a new String array called parameters is created using the query and the value s is changed so that it includes the added string.

## Part 2
* Failure-Inducing Input: 
```
@Test
public void testReversedInPlace1() {
    int[] input1 = {1, 2, 3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[] {3, 2, 1}, input1);
}
```
* Non-Failure-Inducing Input:
```
@Test
public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
}
```
* Symptoms:

![testReversedInPlace1](https://user-images.githubusercontent.com/32721916/215294127-9b30d070-6a2f-4dbe-b017-fa529842575a.png)

![testReverseInPLace](https://user-images.githubusercontent.com/32721916/215294388-5af7c13e-c13c-494a-a343-14ebedf11f99.png)
* The Bug: reverseInPlace would only reverse half the list.
* Before:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = arr[arr.length - i - 1];
    }
}
```
* After:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length / 2; i += 1) {
        int temp = arr[i];
        arr[i] = arr[arr.length - i - 1];
        arr[arr.length - 1 - i] = temp;
    }
}
 ```
This fix addresses the issue because it swaps corresponding values in the list so that they aren't lost (like before). It also loops for only half the list to prevent values from swapping back.

## Part 3
Something I learned from lab in week 2 was how to create servers that actually did something. Before this, I never understood how search engines worked or what their URLs meant. After making my own version of a search engine, it made a lot more sense and I understood more about how it works.
