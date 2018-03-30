---
layout: post
title:  "Unity - Smooth sprite animation"
date:   2018-03-29
desc: "Showing sprite animations with minimal spritesheets"
keywords: "unity,gamedesign,pixel,sprites,pixelated,animations"
categories: [Unity,C#]
tags: [Unity,C#]
icon: icon-csharp
---
<img src="/static/assets/img/blog/birdwalk1.gif" alt="Sprite animation with Animator" style="width: 500px;">

Using Unity's Animator, and static sprite images, we can move sprites in a much cleaner and efficient way than drawing individual sprites for a spritesheet.

<img src="/static/assets/img/blog/birdwalk1ex.jpg" alt="Sprite with joints setup" style="width: 500px;">

The structure of the leg components are: <br><br>
joint<br>
|-upperleg sprite  <br>
&nbsp; |-joint2  <br>
&nbsp; &nbsp; &nbsp; |-lowerleg sprite  <br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |-joint3  <br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |-foot sprite  <br>
<br>
With this structure, we can keyframe the rotations of each joint gameObject to get a walking effect. Because each leg segment and joint is a child of the previous, rotating the joints will keep the leg stuck together nicely.
---
