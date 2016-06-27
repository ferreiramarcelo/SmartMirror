SmartMirror
===========

Motion controlled SmartMirror showing time and temperature in background with the possibility of adding any widget to the menu.
The camera is behind the two-way mirror to get the best possible look. The screen and camera are managed by a raspberry pi.
The motion is managed by a server running in python with OpenCV, the server web is in NodeJS.<br><br>

**Preview**

Showing the display of the main menu and a use case on the widget Cinema (movie times of my local theater)
<p align="center">
  <img src="/docs/SmartMirror_DisplayMenu_Preview.gif"/>       <img src="/docs/SmartMirror_Widget_Preview.gif"/>
</p>


<br>
**Capacities**
- Recognition of gestures : palm, thumbs up/down, slide up/down/right/left
- Time and outside temperature
- Widgets :
  - Photo : take a photo and upload it to Dropbox
  - Map : display local Google Map
  - Cinema : movie time of local theater
  - DoodleJump : play the game (hard with the latency)
  - News : show international news
  

<br>
**Debugging**

The motion server can't recognize gestures on a new environment : lights, hand colors... affect the process, that's why by launching
the test.py file and tweak the HSV min/max values and others configs properly you can set it up for your home.
<br>
![Debugging gesture](/docs/SmartMirror_Debug.png)
[Show webm preview](https://gfycat.com/BountifulCanineBushsqueaker)


<br>
**Dependencies**
- Software :
  - OpenCV 2.x
  - Python 3.x
  - NodeJS
- Hardware :
  - [Two Way Mirror](http://fr.aliexpress.com/item/300mm-x-300mm-x-3-0mm-Acrylic-PMMA-Plexiglass-Partial-Translucent-Mirrored-Sheets-for-Infinity-illusion/32398641282.html)
  - Raspberry pi
  - Camera
  
  
<br>
**Notes**

The motion server was made in python to learn the language, but it should have been made in C/C++ to gain execution speed and flowness in the gestures recognitions.
Also, python environment kinda sucks at the moment, the difficulty to set it up for python3 + opencv2 + windows and then linux was exhausting, I don't recommend.
