# Lab Report 4

## Tasks
1. Log into ieng6

```
ssh cs15lwi23afz@ieng6.ucsd.edu <enter>
```

<img width="671" alt="Screenshot 2023-02-27 at 12 31 47 AM" src="https://user-images.githubusercontent.com/32721916/221513020-d4db1302-7eda-4384-958b-7e5518a7e5c8.png">

I ran the command to login to ieng6 but didnt have to enter my password because I had set up a SSH key.
  
2. Clone your fork of the repository from your Github account

```
git clone <ctrl+c> <ctrl+v> git@github.com:osheentikku/lab7.git
```

<img width="650" alt="Screenshot 2023-02-27 at 1 30 06 PM" src="https://user-images.githubusercontent.com/32721916/221689992-18890ffc-654a-4304-a406-f3327d96cf65.png">

I ran the command to clone the lab 7 repo but I used control-c/v to paste the link in.
   
3. Run the tests, demonstrating that they fail

```
cd l<tab>ab7/
<ctrl+c><ctrl+v><enter>
<ctrl+c><ctrl+v> ListExamplesTests <enter>
```

<img width="1131" alt="Screenshot 2023-02-27 at 12 17 25 PM" src="https://user-images.githubusercontent.com/32721916/221674912-19acb333-174b-4246-b227-6e85519b52f9.png">

I used tab to autocomplete the directory name for cd and the file name when running the test case. I used control-c/v to paste the code to run the java test cases because it was faster than typing it all out. 
  
4. Edit the code file to fix the failing test

```
nano L<tab>istExamples.java <enter>
<ctrl+w><scroll><up><up><up><up><up><up><up><up><up><up><up><backspace> 2
<ctrl+o><enter>
<ctrl+x>
```

<img width="950" alt="Screenshot 2023-02-27 at 12 09 16 PM" src="https://user-images.githubusercontent.com/32721916/221672874-8f330976-5c2c-4a27-8612-6fd4ee81fee0.png">

I used the nano command so I could edit the file from the terminal and used tab to autocomplete the file name. Once I was within the editor, I scrolled down to get to the line I needed to edit and then used the arrow keys to get to the exact spot. Once I was done, I saved and exited the editor using control+o/x.
  
5. Run the tests, demonstrating that they now succeed

```
<up><up><enter>
<up><up><up><enter>
```

<img width="1131" alt="Screenshot 2023-02-27 at 12 23 20 PM" src="https://user-images.githubusercontent.com/32721916/221677130-bc95d237-f37f-4cb4-a748-3f465c531090.png">

I used the up arrow keys to access the javac and java commands for ListExamplesTests since I had already run them once and they were in my command history.
  
6. Commit and push the resulting change to your Github account

```
git add L<tab>istExamples.java
git commit -m "Update"
git push o<tab>rigin m<tab>ain
```

<img width="650" alt="Screenshot 2023-02-27 at 1 34 02 PM" src="https://user-images.githubusercontent.com/32721916/221690735-31d15bb2-cc39-49f0-b745-d70f16f0548d.png">

I used the appropriate git commands to commit and push ListExamples.java. 
