---
layout: post
title: "Developer Diary - Inspire"
comments: true
description: "A diary keeping track of my development process with Inspire"
keywords: "iOS, developer diary, inspire, image, song"
---

[Link to code](https://github.com/minhhoangtcu/Inspire)

I love photography. But, I do not enjoy it so much when I am out ideas on the field. Telling the model to stand still for me to think and walk around could become really awkward. Somtimes, the "feeling" just does not flow into us. This project serves to solve that issue.

## Getting the images
Because I often get stuck when taking portraits and since I am making an application for photographers with similar issue, **the app will request and collect only different kinds of portraits.** But, what are the problems with apps that are already on the Apple Store? Why can't I just use them and stop reinventing the wheel?

### Why current apps are not working?
Let's inspect both the content and the GUI of some of the most popular apps currently on Apple Store.

{:.center}
#### Instagram

{:.center}
![Instagram Screenshoot of beautiful images][screen-instagram]

Beautiful, isn't it? No. It is not going work.

* Professionals do not post their photographs here and when they do, the quality is horrible. We cannot zoom in and most of the images are rectangular (I will save the argument on why rectangular is not favourable).

* Also, there is no way to see the camera EXIF information. When most photographers check a photo, they immedietely look for the shuttle speed, aperature, etc ([here is a professional suggesting how important EXIF is in his series](https://www.youtube.com/playlist?list=PL5D68881416D27814)). Instagram does not offer this feature.

* Exploring on instagram is a no no. You can try and search for the tag "portrait", the results are just teenagers taking selfies. Even if we use instagram's API to filter out the result, the two above problems still exist.

(to be cont)

## Suggesting songs

[screen-instagram]: ../../image/inspire/screen-instagram.png
{: width="450px"}