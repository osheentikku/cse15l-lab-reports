### Lab Report 2

## Part 1
Here is the code for StringServer:
![code](https://user-images.githubusercontent.com/32721916/215285325-430fe6f6-41fa-4397-a812-60a249be6bf8.png)

1. When adding the word "Hello":
![addHello](https://user-images.githubusercontent.com/32721916/215285381-85b0a984-1a18-4bba-8338-42a858e76319.png)
* Calls: ```handleRequest```
* Relevant Arguments: ```URI url```
* Values of Relevant fields: ```parameters = [s, Hello]; s = "Hello \n"```
* Changed Values: From this specific request, a new String array called parameters is created using the query and the value s is changed so that it includes the added string.

2. When adding the word "Goodbye":
3. ![addGoodbye](https://user-images.githubusercontent.com/32721916/215285963-ff1e2b12-25bd-4aaa-8c4d-ee41f7887238.png)
* Calls: ```handleRequest```
* Relevant Arguments: ```URI url```
* Values of Relevant fields: ```parameters = [s, Goodbye]; s = "Hello \n Goodbye \n"```
* Changed Values: From this specific request, a new String array called parameters is created using the query and the value s is changed so that it includes the added string.

## Part 2
* Failure-Inducing Input: 
```
@Test
public void testReversedSimple() {
  int[] input = {1, 2, 3};
  input = ArrayExamples.reversed(input);
  assertArrayEquals(new int[] {3, 2, 1}, input);
}
```

## Part 3
Something I learned from lab in week 2 was how to create servers that actually did something. Before this, I never understood how search engines worked or what their URLs meant. After making my own version of a search engine, it made a lot more sense and I understood more about how it works.
