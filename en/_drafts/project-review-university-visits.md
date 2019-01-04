# Project Review: university visits

## What This Project Is And Why I Did It

This is my first complete project. It has two purposes: providing admissions data to potential new students and scheduling university visits for first-year students. 

I did this project as a competence test when I joined Hongmantang Studio. At the time some third-party websites provided admissions data to help potential new students decide whether they should apply to a university. Those websites tried to collect admissions data from as many universities as possible. Thus, they did not have enough details for each university. We wanted to create a system that could show enough details about the admissions data for our university. At the same time, since the university does not have any visitor-oriented events, our studio has a tradition of inviting freshmen to visit before the beginning of the new school year. We used to ask them to reserve spots by replying to a forum. Soon it became too complex since some students asked questions or chatted with each other in the same forum, making it difficult for us to collect the reservations. In the end, we decided to develop a separate website to accept reservations.

We decided to use PHP as the programming language and MySQL as the database because that’s the only production environment our studio had at that time. This actually limited our choices, so we switched to the Linux and Docker environment. That gave us more options.

## How I Did The Project

This project was a big challenge for me because, as I mentioned in another post, I only knew some very basic knowledge about PHP such as how to write ```<?php echo "Hello World"; ?>```, and I had no knowledge of the database and specifically, MySQL. 

One of my mentors, SpecialCyCi, introduced me a framework called ThinkPHP, which is an object-oriented framework for PHP that supports MySQL as a database. He promised me that it would be easier to use a framework instead of beginning from scratch since a framework already finishes many details for us, making it possible for us to focus on our project. I spent about one week reading the whole documents of ThinkPHP and following the tutorials to write some simple code.

It was July, and the results of the National College Entrance Examination (NCEE) would come out soon. Since new students would begin to search admission data and apply for universities I did not have enough time to finish the project. 

I downloaded data in excel format from admission website and imported it to the database by using `phpMyAdmin`. I knew I should write a user-friendly interface for importing so that future developers could import the data directly instead of using third-party tools. However, I didn’t have the knowledge at the time. I fixed this problem the next year when we needed to reuse the system.

The next challenge was the algorithm. I wanted to extract all the colleges and majors from the data, find their connections, and combine similar majors. This is not difficult for me now. A nest iteration and some regular expression, or even a library can solve this problem easily. But four years ago, before I even knew the definition of an algorithm, the problem brought me a lot of trouble. The loop never stopped. The results did not format in the way I had wanted. At the end of the day, I decided to write down all of my thoughts on a piece of paper and run the code by hand first. That helped me a lot.

I finished the admission data part one day before the NCEE scores released. Thanks to our fantastic market team, the new tool became famous to students who were planning to apply to the university. In the next few days, I received much feedback and fixed some bugs.

The next part was the visiting reservation system. 

## What I Learned From This Project

Try to use a framework. A good framework can handle all the trivial details so that we only need to focus on the functions themselves. For example, the framework that I used, ThinkPHP, could handle database connections, request routing, interface rendering, etc. Thus, I could begin to code immediately instead of spending a couple of hours to figure out how to connect the database. A good framework can also adapt to different development or production environments so we do not need to worry about moving our application from one environment to another.

Try to read documents. I know there are many tutorials that can help us begin to program in less than ten minutes. However, reading the official documents is still important because tutorials will not show you everything. Reading documents at the beginning is better than struggling with something first and then finding the needed documents.

Try to learn algorithms. I did not realize the importance of algorithms before I took the algorithms course. I always thought that if the computer was fast enough, it could solve every problem by itself.

Try to cache everything.

Try not to rely on the frameworks.