# Lab Report 4 Week 8: Testing

This lab will test three snippets of code against my current Markdown Parser and against another group's Markdown Parser. 

Here is a link to mine: [mine](https://github.com/annika484/markdown-parser/blob/main/MarkdownParse.java)

And here is a link to the code I reviewed: [reviewed](https://github.com/henrigy/markdown-parser/blob/main/MarkdownParse.java)
## Snippet 1
Here is what the code is supposed to produce in Snippet 1:

<img width="168" alt="Screen Shot 2022-05-30 at 9 34 42 PM" src="https://user-images.githubusercontent.com/103288525/171093514-9cee6a57-3ccc-4c1f-ab3b-79b86587cf77.png">

Here is the test that I used:

<img width="780" alt="Screen Shot 2022-05-30 at 9 47 47 PM" src="https://user-images.githubusercontent.com/103288525/171094824-2b2c644f-995e-4bb4-88a3-cb846c00f74f.png">

Here is what my MarkdownParse ran:

<img width="1031" alt="Screen Shot 2022-05-30 at 9 48 30 PM" src="https://user-images.githubusercontent.com/103288525/171094925-51d48291-05db-415b-bc07-c3181e59b053.png">

Here is what the code I reviewed ran:

<img width="1114" alt="Screen Shot 2022-05-30 at 9 57 22 PM" src="https://user-images.githubusercontent.com/103288525/171095913-ed779a85-6294-4392-8a53-092d468a6840.png">

I think there is a relatively small code change that will be able to fix the first problem in my code, not including links with a tick in front. 
This is because I already implemented the code which will not include links with an exclamation point in front.
However, the second problem that my code runs into is not picking up on the ucsd.edu link. 
This link contains an extra closed bracket, and to fix this issue I would have to create a way to count the brackets. 
This would take longer, and I'm not certain all the changes would fit within 10 lines of code.

## Snippet 2
Here is what the code is supposed to produce in Snippet 1:

<img width="215" alt="Screen Shot 2022-05-30 at 9 36 34 PM" src="https://user-images.githubusercontent.com/103288525/171093723-e156cd4c-5bd3-4596-8afa-f87dc3def081.png">

Here is the test that I used:

<img width="763" alt="Screen Shot 2022-05-30 at 10 15 42 PM" src="https://user-images.githubusercontent.com/103288525/171097893-ff302808-87bc-4b38-9233-51f70e9ea0a4.png">

Here is what my MarkdownParse ran:

<img width="847" alt="Screen Shot 2022-05-30 at 10 16 16 PM" src="https://user-images.githubusercontent.com/103288525/171097986-a4e93b09-b3ca-49d3-9056-447201c138af.png">

Here is what the code I reviewed ran:

<img width="962" alt="Screen Shot 2022-05-30 at 10 42 24 PM" src="https://user-images.githubusercontent.com/103288525/171100990-ba1a187b-03e2-4503-ab3b-2d904874ff4d.png">

To change this code, I would count the brackets to ensure that what is within the brackets is correctly accounted for, even if it
is more brackets. This possibly could take less than 10 lines of code. 

## Snippet 3
Here is what the code is supposed to produce in Snippet 1:

<img width="556" alt="Screen Shot 2022-05-30 at 9 37 29 PM" src="https://user-images.githubusercontent.com/103288525/171093835-0079540e-5d17-4848-bae0-bb6bc3bddb25.png">

Here is the test that I used:

<img width="940" alt="Screen Shot 2022-05-30 at 10 53 20 PM" src="https://user-images.githubusercontent.com/103288525/171102304-ddcec6dd-5aed-4a16-8f59-af704d13b2fa.png">

Here is what my MarkdownParse ran:

<img width="654" alt="Screen Shot 2022-05-30 at 10 53 03 PM" src="https://user-images.githubusercontent.com/103288525/171102276-c8704eea-1f5d-463c-8f8c-e4d2a00e777d.png">

Here is what the code I reviewed ran:

<img width="1013" alt="Screen Shot 2022-05-30 at 10 54 09 PM" src="https://user-images.githubusercontent.com/103288525/171102393-22eaa3e7-7ec6-4a48-8272-babe7a89065b.png">

My code broke because of an out of bounds error. I would have to fix that first, then get down to incorporating links that traverse different lines. 
I am not sure exactly how long it will take, but I think I could do it in under 10 lines. 


Thank you for reading my code! 
