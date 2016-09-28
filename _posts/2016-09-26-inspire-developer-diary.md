---
layout: post
title: "Developer Diary - Inspire"
comments: true
description: "A diary keeping track of my development process with Inspire"
keywords: "iOS, developer diary, inspire, image, song"
---

[Link to code](https://github.com/minhhoangtcu/Inspire)

I love photography. But, I do not enjoy it so much when I am out ideas on the field. Telling the model to stand still for me to think and walk around could become really awkward. Somtimes, the "feeling" just does not flow into us. This project serves to solve that issue.

# Table of Content
1. [Logic Overview](#logic-overview)
  * [Getting the images](#getting-the-images)
    1. [Why current apps are not working?](#why-current-apps-are-not-working)
  * [Suggesting songs](#suggesting-songs)


# Logic Overview

## Getting the images
Because I often get stuck when taking portraits and since I am making an application for photographers with similar issue, **the app will request and collect only different kinds of portraits.** But, what are the problems with apps that are already on the Apple Store? Why can't I just use them and stop reinventing the wheel?

### Why current apps are not working?
Let's inspect both the content and the GUI of some of the most popular apps currently on Apple Store.

#### Instagram

{:.center}
![Instagram Screenshoot of beautiful images][screen-instagram]

Beautiful, isn't it? No. It is not going work.

Firstly, professionals do not post their photographs here and when they do, the quality is horrible. We cannot zoom in and most of the images are rectangular (I will save the argument on why rectangular is not favourable for later).

Also, there is no way to see the camera EXIF information. When most photographers check a photo, they immedietely look for the shuttle speed, aperature, etc ([here is a professional suggesting how important EXIF is in his series](https://www.youtube.com/playlist?list=PL5D68881416D27814)). Instagram does not offer this feature.

Exploring on instagram is a no no. You can try and search for the tag "portrait", the results are just teenagers taking selfies. Even if we use instagram's API to filter out the result, the two above problems still exist.

#### Flickr
Flickr faces problems similarly to Instagram. Although more professional post their photographs on here and we can actually see the EXIF information. It is not easy to access the EXIF info, we have to navigate through another screen to read more information. I want to design an application that displays the photo with the EXIF information.

Also, Flickr does not really offer an option for photographers to discover images. There is a feature that lists all trending tags. But, I do not want trending stuff, I just want to look for a specific set of stuff. In this case, we are trying to find only portraits.

Since Flickr still has some decent photographs and EXIF information, it is still a good source for inspiration. In fact, our app will ultilize Flickr's API and collect photos from here. But, we will have to add some filter to get a good image.

#### 500px

{:.center}
![500px Screenshoot of beautiful categories][screen-500px]

500px is my favourite. Why? It actually categorizes the pictures! Also, the quality of the photographs is absolutely stunning. Unfortunately, I cannot access the EXIF data without going to another screen. 500px is close, but, for our taste, it is not close enough. In our app, we will have these categories and also use their API to get the pictures.

#### EyeEm

EyeEm is actually a little bit special. It focuses on suggesting users to explore specific photographers or albums based on our interests. So, machine learning is definately heavily involved in there. Since this is the main feature of EyeEm, it does not the easily accessible categories like what 500px does. However, EyeEm has a very interesting way to show image:

{:.center}
![EyeEm Screenshoot of tags with photo][screen-eyeem]

EyeEm displays a picture's tags below the picture. This is semi helpful because sometimes we can see the information of the camera. For example, in the image above, we instantly know that it is captured with a Sony A7 and at 55mm. But, we do not really want to see all those information. Firstly, it is distracting. There are too many taggs. If I were to design the application (showing tags only), I would show only a few of them. And, I will never show the obvious tags. "Girl", "cute", and "portrait" are not neccessary. Without reading the tags, I am very sure that I am seeing a girl already. Anyway, displaying helpful information is what our app is going for.

## Suggesting songs

[screen-instagram]: ../../image/inspire/screen-instagram.png 
{: width="450px"}

[screen-500px]: ../../image/inspire/screen-500px.png 
{: width="450px"}

[screen-eyeem]: ../../image/inspire/screen-eyeem.png 
{: width="450px"}