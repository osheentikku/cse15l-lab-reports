# Lab Report 4

## Tasks
1. Log into ieng6
```
ssh cs15lwi23afz@ieng6.ucsd.edu
```
<img width="671" alt="Screenshot 2023-02-27 at 12 31 47 AM" src="https://user-images.githubusercontent.com/32721916/221513020-d4db1302-7eda-4384-958b-7e5518a7e5c8.png">
I ran the command to login to ieng6 but didnt have to enter my password because I had set up a SSH key.

2. Clone your fork of the repository from your Github account
```
git clone <ctrl+c> <ctrl+v> https://github.com/osheentikku/lab7
```
<img width="685" alt="Screenshot 2023-02-27 at 12 35 12 AM" src="https://user-images.githubusercontent.com/32721916/221513937-d910e5ff-408b-426f-90ab-0007d444e434.png">
I ran the command to clone the lab 7 repo but I used control-c/v to paste the link in.

3. Run the tests, demonstrating that they fail
```
cd l<tab>ab7/
<ctrl+c><ctrl+v> javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
<ctrl+c><ctrl+v> java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore L<tab>istExamplesT<tab>est.java
```
<img width="1221" alt="Screenshot 2023-02-27 at 12 44 51 AM" src="https://user-images.githubusercontent.com/32721916/221515920-1ccde639-f119-4fe2-a90a-ae8daf87c727.png">
I used tab to autocomplete the directory name for cd and the file name when running the test case. I used control-c/v to paste the code to run the java test cases because it was faster than typing it all out.

4. Edit the code file to fix the failing test
```
nano L<tab>istExamples.java
```



5. Run the tests, demonstrating that they now succeed
```
```

6. Commit and push the resulting change to your Github account (you can pick any commit message!)
```
git commit
git push
```
