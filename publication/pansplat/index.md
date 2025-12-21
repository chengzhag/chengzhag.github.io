---
title: "PanSplat: 4K Panorama Synthesis with Feed-Forward Gaussian Splatting"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- admin
- Haofei Xu
- Qianyi Wu
- Camilo Cruz Gambardella
- Dinh Phung
- Jianfei Cai

# # Author notes (optional)
# author_notes:
# - "Equal contribution"
# - "Equal contribution"
# - "Equal contribution"

date: "2024-12-12T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: IEEE Conference on Computer Vision and Pattern Recognition
publication_short: CVPR 2025

abstract: ""

# Summary. An optional shortened abstract.
summary: We present PanSplat, a generalizable, feed-forward approach that efficiently supports resolution up to 4K (2048 × 4096).

tags:
- Deep Learning
- Novel View Synthesis
- Panorama

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
links:
- name: arXiv
  url: 'https://arxiv.org/abs/2412.12096'

url_pdf: ''
url_code: 'https://github.com/chengzhag/PanSplat'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: 'https://youtu.be/R3qIzL77ZSc'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Comparison with MVDiffusion'
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

## <div class="publication-header">CVPR 2025</div>


<div class="publication-header">
  <a href="https://chengzhag.github.io/" target="_blank">Cheng Zhang</a>
  <sup>1,2</sup>
  &nbsp; &nbsp;
  <a href="https://haofeixu.github.io" target="_blank">Haofei Xu</a>
  <sup>3</sup>
  &nbsp; &nbsp;
  <a href="https://wuqianyi.top" target="_blank">Qianyi Wu</a>
  <sup>1</sup>
  <!-- &nbsp; &nbsp; -->
  <br />
  <a href="https://www.researchgate.net/profile/Camilo-Cruz-Gambardella" target="_blank">Camilo Cruz Gambardella</a>
  <sup>1,2</sup>
  &nbsp; &nbsp;
  <a href="https://dinhphung.ml" target="_blank">Dinh Phung</a>
  <sup>1</sup>
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
  <a href="https://building4pointzero.org" target="_blank">Building 4.0 CRC, Caulfield East, Victoria, Australia</a>
  &nbsp; &nbsp;
  <sup>3</sup>
  <a href="https://ethz.ch/en.html" target="_blank">ETH Zurich</a> 
  <!-- <br /> -->
</div>

<center>
  <!-- <a href="#" class="btn btn-outline-primary js-cite-modal" data-filename="cite.bib">
  Cite
  </a> -->
  <a href="https://github.com/chengzhag/PanSplat" class="btn btn-outline-primary" target="_blank">
  Code
  </a>
  <!-- <a href="https://www.youtube.com/watch?v=Kg0du7mFu60" class="btn btn-outline-primary" target="_blank">
  YouTube
  </a>
  <a href="https://www.bilibili.com/video/BV1By4y1g7c5/" class="btn btn-outline-primary" target="_blank">
  bilibili
  </a> -->
  <a href="https://arxiv.org/abs/2412.12096" class="btn btn-outline-primary">
  arXiv
  </a> 
  <a href="https://arxiv.org/pdf/2412.12096" class="btn btn-outline-primary">
  Paper
  </a>
</center>


---
## Short Video

{{< youtube R3qIzL77ZSc >}}

---

## Abstract

With the advent of portable 360° cameras, panorama has gained significant attention in applications like virtual reality (VR), virtual tours, robotics, and autonomous driving.
As a result, wide-baseline panorama view synthesis has emerged as a vital task, where high resolution, fast inference, and memory efficiency are essential.
Nevertheless, existing methods are typically constrained to lower resolutions (512 × 1024) due to demanding memory and computational requirements.
In this paper, we present **PanSplat**, a generalizable, feed-forward approach that efficiently supports **resolution up to 4K** (2048 × 4096).
Our approach features a tailored spherical 3D Gaussian pyramid with a Fibonacci lattice arrangement, enhancing image quality while reducing information redundancy.
To accommodate the demands of high resolution, we propose a pipeline that integrates a hierarchical spherical cost volume and Gaussian heads with local operations, enabling two-step deferred backpropagation for memory-efficient training on a single A100 GPU.
Experiments demonstrate that PanSplat achieves state-of-the-art results with superior efficiency and image quality across both synthetic and real-world datasets.

---
## Full Video

{{< youtube 77G9AQkweg0 >}}

---
## Pipeline

{{< figure width=80% src="pipeline.png" caption="Our proposed PanSplat pipeline. Given two wide-baseline panoramas, we first construct a hierarchical spherical cost volume using a Transformer-based FPN to extract feature pyramid and 2D U-Nets to integrate monocular depth priors for cost volume refinement. We then build Gaussian heads to generate a feature pyramid, which is later sampled with Fibonacci lattice and transformed to spherical 3D Gaussian pyramid. Finally, we unproject the Gaussian parameters for each level and view, consolidate them into a global representation, and splat it into novel views using a cubemap renderer. For simplicity, intermediate results of only a single view are shown." >}}

---
## Interactive Demo

{{< youtube 9bKZA2zxAbw >}}
(Best viewed on a desktop browser or Youtube app.)

---
## Results

{{< figure width=90% src="teaser.png" >}}
