---
title: "PanFlow: Decoupled Motion Control for Panoramic Video Generation"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- admin
- Hanwen Liang
- Donny Y. Chen
- Qianyi Wu
- Konstantinos N. Plataniotis
- Camilo Cruz Gambardella
- Jianfei Cai

# # Author notes (optional)
# author_notes:
# - "Equal contribution"
# - "Equal contribution"
# - "Equal contribution"

date: "2025-12-21T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: AAAI Conference on Artificial Intelligence
publication_short: AAAI 2026

abstract: ""

# Summary. An optional shortened abstract.
summary: "PanFlow is a framework for controllable 360° panoramic video generation that decouples motion input into two interpretable components: rotation flow and derotated flow."

tags:
- Deep Learning
- Video Generation
- Panorama
- Motion Control

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
links:
- name: arXiv
  url: 'https://arxiv.org/abs/2512.00832'

url_pdf: ''
url_code: 'https://github.com/chengzhag/PanFlow'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: 'https://youtu.be/sFTWwlHjNtg'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Application on panoramic video editing'
  focal_point: Center
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []
# - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: "" # example
---

<!-- {{% callout note %}}
Click the *Cite* button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Supplementary notes can be added here, including [code, math, and images](https://wowchemy.com/docs/writing-markdown-latex/). -->

## <div class="publication-header">AAAI 2026</div>

<div class="publication-header">
  <a href="https://chengzhag.github.io/" target="_blank">Cheng Zhang</a>
  <sup>1,2</sup>
  &nbsp; &nbsp;
  <a href="https://github.com/hw-liang" target="_blank">Hanwen Liang</a>
  <sup>3</sup>
  &nbsp; &nbsp;
  <a href="https://donydchen.github.io" target="_blank">Donny Y. Chen</a>
  <sup>1</sup>
  &nbsp; &nbsp;
  <a href="https://wuqianyi.top" target="_blank">Qianyi Wu</a>
  <sup>1</sup>
  <!-- &nbsp; &nbsp; -->
  <br />
  <a href="https://www.ece.utoronto.ca/people/plataniotis-k-n/" target="_blank">Konstantinos N. Plataniotis</a>
  <sup>3</sup>
  &nbsp; &nbsp;
  <a href="https://www.researchgate.net/profile/Camilo-Cruz-Gambardella" target="_blank">Camilo Cruz Gambardella</a>
  <sup>1,2</sup>
  &nbsp; &nbsp;
  <a href="https://jianfei-cai.github.io" target="_blank">Jianfei Cai</a>
  <sup>1</sup>
</div>

<div class="publication-header">
  <sup>1</sup>
  <a href="https://www.monash.edu" target="_blank">Monash University</a> 
  &nbsp; &nbsp;
  <!-- <br /> -->
  <sup>2</sup>
  <a href="https://building4pointzero.org" target="_blank">Building 4.0 CRC</a>
  &nbsp; &nbsp;
  <sup>3</sup>
  <a href="https://www.utoronto.ca" target="_blank">University of Toronto</a> 
  <!-- <br /> -->
</div>

<center>
  <!-- <a href="#" class="btn btn-outline-primary js-cite-modal" data-filename="cite.bib">
  Cite
  </a> -->
  <a href="https://github.com/chengzhag/PanFlow" class="btn btn-outline-primary" target="_blank">
  Code
  </a>
  <a href="https://www.youtube.com/watch?v=sFTWwlHjNtg" class="btn btn-outline-primary" target="_blank">
  Video
  </a>
  <!-- <a href="https://www.bilibili.com/video/BV1By4y1g7c5/" class="btn btn-outline-primary" target="_blank">
  bilibili
  </a> -->
  <a href="https://arxiv.org/abs/2512.00832" class="btn btn-outline-primary">
  arXiv
  </a> 
  <a href="https://arxiv.org/pdf/2512.00832" class="btn btn-outline-primary">
  Paper
  </a>
</center>


---
## Video

{{< youtube sFTWwlHjNtg >}}

---

## Abstract

Panoramic video generation has attracted growing attention due to its applications in virtual reality and immersive media. However, existing methods lack explicit motion control and struggle to generate scenes with large and complex motions. We propose PanFlow, a novel approach that exploits the spherical nature of <u>pan</u>oramas to decouple the highly dynamic camera rotation from the input optical <u>flow</u> condition, enabling more precise control over large and dynamic motions. We further introduce a spherical noise warping strategy to promote loop consistency in motion across panorama boundaries. To support effective training, we curate a large-scale, motion-rich panoramic video dataset with frame-level pose and flow annotations. We also showcase the effectiveness of our method in various applications, including motion transfer and video editing. Extensive experiments demonstrate that PanFlow significantly outperforms prior methods in motion fidelity, visual quality, and temporal coherence.

---
## Method

{{< figure width="480" src="teaser.png" caption="**Spherical Camera Optical Flow.** The optical flow from a panoramic video (left) can be interpreted as a spherical camera optical flow (right). For complex motion **f**, the camera rotation yields an analytic rotation flow **f**r on the sphere. By decomposing **f** into **f**r and its residual, we obtain a derotated flow **f**d that more clearly captures camera translation and object dynamics." >}}

{{< figure width="1000" src="pipeline.png" caption="**Our proposed PanFlow pipeline.** Given an input image and text prompt, PanFlow uses a decoupled motion from a video as reference to generate a panoramic video. We first estimate a decoupled optical flow from the reference video, of which the derotated flow is used to generate a latent noise with spherical noise warping. The latent noise then serves as a motion condition for a video diffusion transformer with LoRA fine-tuning to generate derotated videos. Finally, the decoupled rotation is accumulated and applied to the generated video frames to recover the full motion." >}}

---
## Applications

<!-- {{< figure width=90% src="editing.gif" >}} -->

By conditioning diffusion on spherical-warped motion noise, PanFlow enables precise motion control, produces loop-consistent panoramas, and supports applications such as motion transfer:

<p align="center">
  <img src="transfer.gif" alt="transfer" width="860">
</p>

and panoramic video editing:

<p align="center">
  <img src="editing.gif" alt="editing" width="860">
</p>
