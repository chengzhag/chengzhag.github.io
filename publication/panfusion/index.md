---
title: "Taming Stable Diffusion for Text to 360° Panorama Image Generation"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- admin
- Qianyi Wu
- Camilo Cruz Gambardella
- Xiaoshui Huang
- Dinh Phung
- Wanli Ouyang
- Jianfei Cai

# # Author notes (optional)
# author_notes:
# - "Equal contribution"
# - "Equal contribution"
# - "Equal contribution"

date: "2024-04-11T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: IEEE Conference on Computer Vision and Pattern Recognition
publication_short: CVPR 2024

abstract: ""

# Summary. An optional shortened abstract.
summary: We introduce a novel dual-branch diffusion model named PanFusion to generate a 360-degree image from a text prompt.

tags:
- Deep Learning
- Image Generation
- Panorama

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
links:
- name: arXiv
  url: 'https://arxiv.org/abs/2404.07949'

url_pdf: ''
url_code: 'https://github.com/chengzhag/PanFusion'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

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


## [<div class="publication-header">CVPR 2024 Highlight</div>](https://cvpr.thecvf.com/Conferences/2024)

<div class="publication-header">
  <a href="https://chengzhag.github.io/" target="_blank">Cheng Zhang</a>
  <sup>1,3</sup>
  &nbsp; &nbsp;
  <a href="https://wuqianyi.top" target="_blank">Qianyi Wu</a>
  <sup>1</sup>
  &nbsp; &nbsp;
  <a href="https://www.researchgate.net/profile/Camilo-Cruz-Gambardella" target="_blank">Camilo Cruz Gambardella</a>
  <sup>1,3</sup>
  &nbsp; &nbsp;
  <a href="https://xiaoshuihuang.github.io" target="_blank">Xiaoshui Huang</a>
  <sup>2</sup>
  <!-- &nbsp; &nbsp; -->
  <br />
  <a href="https://dinhphung.ml" target="_blank">Dinh Phung</a>
  <sup>1</sup>
  &nbsp; &nbsp;
  <a href="https://wlouyang.github.io" target="_blank">Wanli Ouyang</a>
  <sup>2</sup>
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
  <a href="https://www.shlab.org.cn" target="_blank">Shanghai AI Laboratory</a> 
  <!-- <br /> -->
  &nbsp; &nbsp;
  <sup>3</sup>
  <a href="https://building4pointzero.org" target="_blank">Building 4.0 CRC, Caulfield East, Victoria, Australia</a>
</div>

<center>
  <a href="#" class="btn btn-outline-primary js-cite-modal" data-filename="cite.bib">
  Cite
  </a>
  <a href="https://github.com/chengzhag/PanFusion" class="btn btn-outline-primary" target="_blank">
  Code
  </a>
  <!-- <a href="https://www.youtube.com/watch?v=Kg0du7mFu60" class="btn btn-outline-primary" target="_blank">
  YouTube
  </a>
  <a href="https://www.bilibili.com/video/BV1By4y1g7c5/" class="btn btn-outline-primary" target="_blank">
  bilibili
  </a> -->
  <a href="https://arxiv.org/abs/2404.07949" class="btn btn-outline-primary" target="_blank">
  arXiv
  </a> 
  <a href="https://arxiv.org/pdf/2404.07949.pdf" class="btn btn-outline-primary" target="_blank">
  Paper
  </a>
</center>

{{< figure width=90% src="teaser.png" >}}

---
## Abstract
Generative models, e.g., Stable Diffusion, have enabled the creation of photorealistic images from text prompts. Yet, the generation of 360-degree panorama images from text remains a challenge, particularly due to the dearth of paired text-panorama data and the domain gap between panorama and perspective images. In this paper, we introduce a novel dual-branch diffusion model named PanFusion to generate a 360-degree image from a text prompt. We leverage the stable diffusion model as one branch to provide prior knowledge in natural image generation and register it to another panorama branch for holistic image generation. We propose a unique cross-attention mechanism with projection awareness to minimize distortion during the collaborative denoising process. Our experiments validate that PanFusion surpasses existing methods and, thanks to its dual-branch structure, can integrate additional constraints like room layout for customized panorama outputs. Code is available at [https://chengzhag.github.io/publication/panfusion](https://chengzhag.github.io/publication/panfusion).

---
## Pipeline

{{< figure width=80% src="pipeline.png" caption="Our proposed dual-branch PanFusion pipeline. The panorama branch (upper) provides global layout guidance and registers the perspective information to get seamless panorama output. The perspective branch (lower) harnesses the rich prior knowledge of Stable Diffusion (SD) and provides guidance to alleviate distortion under perspective projection. Both branches employ the same UNet backbone with shared weights, while finetuned with separate LoRA layers. Equirectangular-Perspective Projection Attention (EPPA) modules are plugged into different layers of the UNet to pass information between the two branches." >}}


---
## Comparisons

<center>
  {{< gallery album="comp" >}}
</center>

---
## Generalization

<center>
  {{< gallery album="generalization" >}}
</center>
