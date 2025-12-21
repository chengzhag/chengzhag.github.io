---
title: Ball on Small Plate

# Summary for listings and search engines
summary: The project focus on balancing and controlling the movement of a metal ball on a 20cm wide plate, and is capable of setting target coordinate, circle around the center with adjustable radius.

tags:
- Contest
- Control System
- Electronics Design

# Date published
date: "2017-06-04T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: Ball on plate in action. A simple interface is made to adjust the target position and circle radius.
  focal_point: Smart
  preview_only: false

# links:
# - icon: twitter
#   icon_pack: fab
#   name: Follow
#   url: https://twitter.com/georgecushen
url_code: "https://github.com/pidan1231239/ball_on_plate"
url_pdf: ""
url_slides: ""
url_video: "https://youtube.com/watch?v=UgZbSz2ecN0"

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

---
## Introduction

Ball on Small Plate is built with a Raspberry Zero, a camera, two servos, a STM32F103 board, and is capable of setting target coordinate, circling around the center with adjustable radius.
This project is a work of team of 3, which includes [shicaiwei123](https://github.com/shicaiwei123) and [yoyolalala](https://github.com/yoyolalala). 
Code and documents are available [here](https://github.com/pidan1231239/ball_on_plate). Platform details are discussed [here]({{< relref "../ball_on_big_plate" >}}).

---
## Demo

{{< youtube UgZbSz2ecN0 >}}

---
## Mechanical structure

### First version

The 20cm*20cm plate is made of 1mm black glass fiber board. In the first version shown in the video, the plate is covered with white paper to provide more contrast between ball and plate. Below shows the original plate.

{{< figure src="IMG_20170619_162559.jpg" caption="Deisigning the mechanical structure" >}}

The plate is supported with a universal joint in the center and has 2 degrees of freedom. The angle of the plate is controled by two servos with ball joint rods connecting the servos and the plate.

{{< figure src="IMG_20170619_172950.jpg" caption="Installation of plate and two servos" >}}

In this first version. The camera is fixed to the base, which requires extra procedure to segment the plate from background and warp back to squre. This introduces noise to the positioning of the ball, which is the major reason for the jittering in the video. 

{{< figure src="cap_VID_20170624_154918_00_00_02_01.jpg" caption="Installation of camera and Raspberry Pi Zero" >}}

### Second version

By fixing the camera to the plate with carbon fiber tubes, we managed to avoid the noise. The Raspberry Pi 3b is hanged beyond the camera to reduce the load on the servos. The plate itself is also changed to yellow thus no paper is needed. This reduces friction between the ball and the plate.

{{< figure src="8.jpg" caption="Camera is connected to the plate to reduce jitter" >}}

A ring light is installed around the camera for better illumination.

{{< figure src="6.jpg" caption="Camera and LED installation" >}}

Below shows the PCB board installed on the base, which is later used in project [Ball on Big Plate]({{< relref "../ball_on_big_plate" >}}). 

{{< figure src="ball_on_big_plate_pcb.jpg" caption="PCB mother board" >}}
