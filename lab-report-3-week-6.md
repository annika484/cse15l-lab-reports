# Lab Report 3
This lab will cover how to make life easier through streamlining ssh configuration, setting up Github access thorugh ieng6, and copying whole directories using scp -r.

## Streamlining ssh Configuration
To make ssh easier to access, we will write code to automatically call the host and username. 
Here is the exact code that I put into my config file:

<img width="418" alt="Screen Shot 2022-05-16 at 10 13 43 PM" src="https://user-images.githubusercontent.com/103288525/168734325-db90e469-7349-4979-ba49-06949afb93b0.png">

Or again, seen here in my terminal.
<img width="551" alt="Screen Shot 2022-05-16 at 11 06 42 PM" src="https://user-images.githubusercontent.com/103288525/168740481-61f4831a-5433-4916-9f9b-c1272f0e7a84.png">

By writing out the names of the host and user, I no longer have to write out the long ssh cse... anymore. 
Now, here is what it looks like to open the connection:

<img width="635" alt="Screen Shot 2022-05-16 at 10 17 49 PM" src="https://user-images.githubusercontent.com/103288525/168734543-96809c80-4dbc-4379-89a3-a4b5da0c4b8e.png">

Seen here, there is very little typing I have to do. Now it's easy to enter the remote server.

<img width="563" alt="Screen Shot 2022-05-16 at 10 46 41 PM" src="https://user-images.githubusercontent.com/103288525/168737945-16cb1a9c-7c0f-4e4d-8a2d-b7a834e98d8f.png">

From then on, using scp to copy files is much easier!

## Setup Github Access from ieng6
When I use the command, 
``` cd ~/.ssh ```
I can see where my key is stored:

<img width="521" alt="Screen Shot 2022-05-16 at 11 07 41 PM" src="https://user-images.githubusercontent.com/103288525/168740618-6b8ae6b1-d030-4712-9629-b417b9b1aed3.png">

Here is me checking my git status and then pushing my change.
<img width="613" alt="Screen Shot 2022-05-16 at 11 18 11 PM" src="https://user-images.githubusercontent.com/103288525/168742112-9cd3af35-0653-418b-adbf-90e0a01ebd2d.png">

Here is the link with the resulting change: [link](https://github.com/annika484/markdown-parser/commit/cb386d10cba4adb4614627b3f96ffc5d2cc0b578)

Now, because I can access git in my terminal, it is much easier to committ/push/pull changes!

## Copy whole directories with scp -r
Using scp -r, now we can copy more things than just a file. Here is a screenshot of me using this command:

<img width="704" alt="Screen Shot 2022-05-16 at 11 30 00 PM" src="https://user-images.githubusercontent.com/103288525/168743927-0c25b086-f0b8-42c3-b04d-e59cecdee2e4.png">

Now, markdownparse is in the remote server!

<img width="608" alt="Screen Shot 2022-05-16 at 11 30 57 PM" src="https://user-images.githubusercontent.com/103288525/168744083-cf14dbc7-e8d5-4c6e-9fea-69c989bd2200.png">

Here we can see that I can run markedownparse on the remote server by opening it and running it using make test.

<img width="913" alt="Screen Shot 2022-05-16 at 11 32 36 PM" src="https://user-images.githubusercontent.com/103288525/168744351-2b57a343-0e37-438d-a4f7-be86375313ad.png">

Finally, we can combine the scp -r with ssh in order to run them all at the same time!

<img width="952" alt="Screen Shot 2022-05-16 at 11 50 06 PM" src="https://user-images.githubusercontent.com/103288525/168747174-ac3b9887-f3ea-4d1a-bc18-c960a8ac6c6d.png">
<img width="889" alt="Screen Shot 2022-05-16 at 11 50 21 PM" src="https://user-images.githubusercontent.com/103288525/168747220-1a0d64b4-ab02-45f3-8223-590cd9b7dadd.png">


Thank you for reading my lab report, I hope this made making running code smoother!
