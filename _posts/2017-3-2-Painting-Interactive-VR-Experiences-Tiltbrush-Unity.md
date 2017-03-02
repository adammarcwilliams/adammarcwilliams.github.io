---
layout: post
title: Painting Interactive VR Experiences with TiltBrush & Unity
---

Google’s Tilt Brush finally came to the Oculus Rift recently, optimized for Oculus’s Touch Controllers.

If you’ve not had a chance to play with this yet, I highly recommend giving it a whirl. The experience of painting/illustrating 3D scenes in VR is really something, and Tilt Brush makes the process extremely intuitive.

What really piqued my interest though is learning that the developers also open sourced a Tilt Brush Tool Kit. This takes the hassle out of exporting your creations into the Unity 3D game engine, including many of their SFX and Audio Reactive Brushes.

I’ve seen some interesting discussion on weather VR creation tools like Tilt Brush, Quill & Medium could become part of a professional development pipeline and so I decided to investigate.

This isn’t going to be a step by step tutorial but along the way I will link to any resources I used to learn the various technologies so you can tackle similar projects yourself.

As well as being my first time using a Tilt Brush creation in VR, this was also my first time creating a VR application with Oculus Touch Support, so the objectives for this project were as followed.
- Create a scene in Tilt Brush that included elements that react to music.
- Set-Up a Unity VR project using the Oculus, Oculus Avatar & Oculus Platform SDK’s.
- Import the Tilt Brush models into my scene and configure Audio Reactivity.
- Create an interactive object that toggles the music on/off and responds to touch.

Oculus have some great developer documentation that will give you detailed information on each of their SDK's but for the sake of this article, here is a quick overview of what we'll be using each for.

#### Oculus SDK
This is the starting point for developing with Unity and gives you their OVRCamera prefab which represents the headset in VR and gives you access to the touch controllers inputs.

#### Oculus Avatar SDK
This takes the touch controllers one step further and brings proper models that represent your hands in VR (as well as the rest of your avatar should you have a mirror in your scene or multiple players).

#### Oculus Platform SDK
Finally, if you want to replace the default blue Avatar with your users custom one from Oculus Home then this enables you to do just that.

With that out of the way, lets get started.

### Tilt Brush Scene

Suprisingly, I've not found very many detailed guides on using Tilt Brush and the in-app tutorial is just a series of tool tips. This isn't much of a sticking point though as the process is very intuitive so my best advice would be to just get stuck in and see what all the different tools do.

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Well... first attemp with <a href="https://twitter.com/hashtag/TiltBrush?src=hash">#TiltBrush</a> and I&#39;ve managed to make a psychedelic mess 🤣 <a href="https://t.co/iGzaDxqklS">pic.twitter.com/iGzaDxqklS</a></p>&mdash; Adam Marc Williams (@amwcodes) <a href="https://twitter.com/amwcodes/status/834886932651986944">February 23, 2017</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Luckily my second attempt went better and that is what we will be using for this project.

![Tilt Brush Groot]({{ site.baseurl }}/images/tilt-brush-groot.gif)

One tip I can give is that Tilt Brush allows you to bring in reference material such as images or plain 3D models for you to use as guides. Big thank you to Corentin who made this model of [Dancing Groot](https://sketchfab.com/models/90fe6093ac5747b9a59c0b3317f5808c) available to download on SketchFab.
