# Week 4 Lab Report 2

In this lab we learned how to identify bugs using tests and then fixed them. 

## Code Change 1:

Here is the code change:
<img width="1251" alt="Screen Shot 2022-04-24 at 9 30 02 PM" src="https://user-images.githubusercontent.com/103288525/165021510-0ac57a2c-da10-46fc-a037-b02023320143.png">

This is the testing file that caused the code to break:

[Link](https://github.com/annika484/markdown-parser/blob/main/test-file.md)

Here is the symptom that the code was experiencing beforehand:

<img width="613" alt="Screen Shot 2022-04-24 at 9 25 35 PM" src="https://user-images.githubusercontent.com/103288525/165021545-4a914eb5-c0be-479a-b062-5df8a8fcc434.png">

This is what happened:

The symptom showed that the code was getting stuck in a loop, because of the "Out of memory error". When I checked the code I learned the code was continuing to run after there was no more links to be found because it was attempting to run the empty line after the link in the test file. I fixed this by adding a simple if statement, which would break the loop if no more open parentheses were found. 

## Code Change 2:

Here is the code change:
<img width="1235" alt="Screen Shot 2022-04-24 at 10 42 35 PM" src="https://user-images.githubusercontent.com/103288525/165027458-33a2ae8f-877c-4211-87c7-e95b772b9f51.png">

This is the testing file that cause the code to break:

[Link](https://github.com/annika484/markdown-parser/blob/main/testfile2.md)

Here is the symptom that the code was experiencing beforehand:
<img width="706" alt="Screen Shot 2022-04-24 at 10 40 11 PM" src="https://user-images.githubusercontent.com/103288525/165027572-213147ad-bb72-476b-ba70-d626dc9b7a87.png">

This is what happened:
The symptom showed that one of the variables were "-1", meaning they were not present in the rest of the string. Therefore, we must make sure that if this is the case, we stop the code from running. I ended up placing an if statement that ended the while loop if one or multiple of the variables equalled "-1".

## Code Change 3:

Here is the code change:
<img width="1244" alt="Screen Shot 2022-04-24 at 11 05 23 PM" src="https://user-images.githubusercontent.com/103288525/165029812-76b3be02-2063-41ea-bef6-807dd9dc47e2.png">


This is the testing file that cause the code to break:

[Link](https://github.com/annika484/markdown-parser/blob/main/testfile3.md)

Here is the symptom that the code was experiencing beforehand:
<img width="599" alt="Screen Shot 2022-04-24 at 10 55 40 PM" src="https://user-images.githubusercontent.com/103288525/165029892-82120621-2218-4d33-bed0-32e6d541374b.png">


This is what happened:
Here, the symptom doesn't create an error but it provides the incorrect output instead of []. I found that the cause was that there was nothing keeping the code from running without checking if the link name was connected to the link itself. I fixed it by assuring that closing bracket was behind open parentheses. 

Thank you for reading my lab report!
