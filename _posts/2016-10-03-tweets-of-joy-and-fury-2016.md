---
layout: post
title: "Tweets of Joy and Fury 2016"
comments: true
description: "A diary keeping track of my development process with Inspire"
keywords: "iOS, developer diary, inspire, image, song"
---

[Link to code](https://github.com/awernick/TweetsOfJoyAndFury2016) 
*This is a Github of my partner, he linked both the back end and client to it. Please note that, in this blog, I will focus on only the client part*

[Link to Devpost](http://devpost.com/software/tweets-of-joy-and-fury-2016)

Have you ever wondered what people are talking about the 2016 Presidential debates? This iOS application parses and applies sentiment analysis in real time on Tweets related to Trump and Hillary. You can actually see Tweets popping up in your local area in real time!

# Table of Content
1. [Logic Overview](#logic-overview)
	* [Getting the Tweets](#getting-the-tweets)
	* [Displaying the Tweets](#displaying-the-tweets)
2. [Implementation Details/Progresses](#implementation-details/progresses)
	* [Prototyping](#prototyping)
	* [Creating custom info windows](#creating-custome-info-windows)
	* [Displaying all info windows](#displaying-all-info-windows)
	* [Requesting the Tweets](#requesting-the-tweets)


# Logic Overview
In this project, I worked together with two other lovely people. One worked on the backend and the other worked on the data analysis. Thus, I will mostly talk about my work, which is the implementation of the front-end.

## Getting the Tweets

Firstly, we called Twitter's API to get the Tweets. Of course, we had to pass in certain queries and parse the data in certain way. Lastly, we trained our model with Stanford's data  apply sentiment analysis on the Tweets. For getting the result, the client would push its current location of the map along with the radius of the current zoom level to the server, which will send back data accordingly.

## Displaying the Tweets

We liked the idea of having Trump's faces all other the map. Thus, for every negative Tweet about him, there would be an angry Trump on the map. The same idea applies to display happy Trump, sad Hillary, and happy Hillary. So, here they are, feast your eyes:

{:.center}
![Clinton happy][clinton-happy] ![clinton-sad][clinton-sad] ![trump-angry][trump-angry] ![trump-proud][trump-proud]

And, we also wanted to display live Tweets, so that the heads will pop up everytime, which would be really cool!

# Implementation Details/Progresses
I devide this section into multiple milestones. Each problem took considerable amout of time and had a profound impact on the project.

## Prototyping
Learning from my pit fall of my last side project, this time, I need to have an usable prototype.

And, I need it fast! *In the end, it took me 3 hours, which is not ok*

Firstly, we discussed the purpose of the application and determined its features. Then, I began to draw some sketches and reviewed with the team. Normally, during this prototyping progress, people did not create an entire design from nothing. I highly recommend using Photoshop/Keynote to modify designs on [pttrns](http://pttrns.com/) and wrap the entire process with [inVision](https://www.invisionapp.com/).

Here are the raw designs and their modifications side by side:

{:.center}
![infoscreen][infoscreen] ![infoscreen-processed][infoscreen-processed]


[clinton-happy]: ../../image/tweets/clinton-happy.png 
{: width="100px"}

[clinton-sad]: ../../image/tweets/clinton-sad.png 
{: width="100px"}

[trump-angry]: ../../image/tweets/trump-angry.png 
{: width="100px"}

[trump-proud]: ../../image/tweets/trump-proud.png 
{: width="100px"}



[infoscreen-processed]: ../../image/tweets/infoscreen-processed.png 
{: width="350px"}

[mapscreen-processed]: ../../image/tweets/mapscreen-processedpng 
{: width="350px"}

[infoscreen]: ../../image/tweets/infoscreen.jpg
{: width="350px"}

[mapscreen]: ../../image/tweets/mapscreen.jpg 
{: width="350px"}