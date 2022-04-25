# Week 4 Lab Report 2

In this lab we learned how to identify bugs using tests and then fixed them. 

## Code change 1:

Here is the code change:
<img width="1251" alt="Screen Shot 2022-04-24 at 9 30 02 PM" src="https://user-images.githubusercontent.com/103288525/165021510-0ac57a2c-da10-46fc-a037-b02023320143.png">

This is the testing file that caused the code to break:

[Link](https://github.com/annika484/markdown-parser/blob/main/test-file.md)

Here is the symptom that the code was experiencing beforehand:

<img width="613" alt="Screen Shot 2022-04-24 at 9 25 35 PM" src="https://user-images.githubusercontent.com/103288525/165021545-4a914eb5-c0be-479a-b062-5df8a8fcc434.png">

This is what happened:

The symptom showed that the code was getting stuck in a loop, because of the "Out of memory error". When I checked the code I learned the code was continuing to run after there was no more links to be found because it was attempting to run the empty line after the link in the test file. I fixed this by adding a simple if statement, which would break the loop if no more open parentheses were found. 
