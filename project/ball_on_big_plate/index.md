---
title: Ball on Big Plate

# Summary for listings and search engines
summary: The project focus on balancing and controlling the movement of a metal ball on a 65cm wide plate, and is a work of 3 team-mates which get us first prize in 2017NUEDC.

tags:
- Contest
- Control System
- Electronics Design

# Date published
date: "2017-09-03T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: The complete work
  focal_point: Smart
  preview_only: false

# links:
# - icon: twitter
#   icon_pack: fab
#   name: Follow
#   url: https://twitter.com/georgecushen
url_code: "https://github.com/pidan1231239/ball_on_big_plate"
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

gallery_item:
- album: xian
  image: IMG_20170831_144038_01.jpg
  caption: Final test in Jiaotong University
- album: xian
  image: IMG_20170830_175531.jpg
  caption: On the way to the final test
- album: xian
  image: IMG_20170831_163601.jpg
  caption: DaYanTa station of Xi'an metro Line 3
- album: xian
  image: IMG_20170831_164508.jpg
  caption: Dayan Tower of Xi'an
- album: xian
  image: IMG_20170831_190316.jpg
  caption: Mutton soup with bread of Xi'an
---

---
## Introduction

This project is a work of team of 3, which includes [shicaiwei123](https://github.com/shicaiwei123) and [zianglei](https://github.com/zianglei). 
The preparations of the contest are done with the help of [yoyolalala](https://github.com/yoyolalala).
I was responsible for building mechanical structures and embedded programming (i.e. STM32, Raspberry Pi).
We are lucky to have received the first prize in [2017NUEDC](https://www2.renesas.cn/zh-cn/about/university-program/nuedc/2017.html). 
The final work has been handed in to our school thus details will not be provided. 
However, code and document can be found [here](https://github.com/pidan1231239/ball_on_big_plate). 

> The ball-on-plate system is a promoted version of the traditional ball-on-beam control problem. The problem consists of a plate which its deviation can be manipulated in two perpendicular directions. The goal is to carry the ball moving on the plate to a desired position, that is to control a freely rolling ball on a specific position or moving on a trajectory on the plate. - [Modelling and Control of Ball-Plate System](http://web.engr.illinois.edu/~khashab2/files/2011_LinearControl/16.pdf)
> {{< figure src="ball-on-plate_system.png" caption="Ball-on-plate system" >}}

Specifically in this project, according to the contest requirements, the system is supposed to move a ball between any two of nine evenly distributed circles and avoids the others. The plate must have a size around 65cm*65cm. The [document](滚球控制系统（B题）.pdf) shows the distribution of the circles.

---
## The Contest

[NUEDC](https://www2.renesas.cn/zh-cn/about/university-program/nuedc/2017.html) is one of the largest electronic design contest for undergraduate students in China. The contest lasts three and a half days. More than ten topics of four types including control, measurement, communication and power are published in the first day morning, indicating the start of the contest. Participants usually prepare for a long time before the contest. We attended the contest in 2017 starting from August 9th to 12th. Our team started the preparation four months in advance. 

Although I had got some experience with programming, I barely knew the basics of control system. However, I chose this type of topic just in the interest of it.

In the preparation process, we learned from five projects, three of which are listed below.
- [Rotary Inverted Pendulum]({{< relref "../rotary_inverted_pendulum" >}})
- [Ball on Beam]({{< relref "../ball_on_beam" >}})
- [Ball on Small Plate]({{< relref "../ball_on_small_plate" >}})

Sadly, no video demo was taken for the limit of time.

---
## Platform

- Raspberry Pi Zero and Raspberry Pi 3b with OpenCV installed
- STM32F103 minimum system board
- PC with Visual Studio and VisualGDB installed

The Raspberry Pi is developed with C++ using Raspberry Pi toolchain provided by [VisualGDB](https://visualgdb.com/) (tutorial [here](https://visualgdb.com/tutorials/raspberry/crosscompiler/)).
It deals with the machine vision tasks and sends the results to STM32 through UART.

The STM32 is developed with C++ language using Arm toolchain provided by [VisualGDB](https://visualgdb.com/) (tutorial [here](https://visualgdb.com/tutorials/arm/stm32/)).
A C++ API for STM32 ([Ebox](https://github.com/eboxmaker/eBox_STM32F1)) was used as a replacement of ardunio, which is not allowed in the contest.

---
## Mechanical structure

The final work uses a PCB motherboard (designed by [shicaiwei123](https://github.com/shicaiwei123)) same as [Ball on Small Plate project]({{< relref "../ball_on_small_plate" >}}) to connect modular electronic parts. 

{{< figure src="3.jpg" caption="PCB mother board" >}}

The 65cm*65cm plate is made of laminated balsa wood board.

{{< figure src="ball_on_big_plate_camera_support.jpg" caption="The plate" >}}

We design metre-shaped ribs to further reinforce the plate.
We follow [Ball on small plate]({{< relref "../ball_on_small_plate" >}}) to support the plate with a universal joint in the center and drive the board with two servos using ball joint rods as connection.

{{< figure src="ball_on_big_plate_under_the_plate.jpg" caption="Under the plate" >}}

Design documents of the reinforcing ribs are also available [here](https://github.com/pidan1231239/ball_on_big_plate).

{{< figure src="650板加强筋激光切割.dwg.png" caption="Reinforcing ribs" >}}

{{< figure src="ball_on_big_plate_universal_joint.jpg" caption="Cardan joint" >}}

{{< figure src="ball_on_big_plate_ball_rod.jpg" caption="Servo with connecting rod" >}}

The camera is supported by carbon fiber tubes like in [Ball on small plate]({{< relref "../ball_on_small_plate" >}}). 
And the same ring light is installed around the camera to provide better illumination.

{{< figure src="ball_on_big_plate_led.jpg" caption="LED around camera" >}}

The Raspberry Pi 3b is hanged beyond the camera to reduce the load on the servos.

{{< figure src="featured.jpg" caption="The complete work" >}}

The final work is packed with cardboard then submitted to the competition organizer.

{{< figure src="IMG_20170812_225850_001.jpg" caption="Complete work packed with cardboard, kinda like a house" >}}

---
## Final test

After a successful test in front of the judges of Sichuan division, follwed by a basic on-site electronic design test, we went to Xi'an for the final test. Below shows some photos taken along the trip.

{{< gallery album="xian" >}} 
