---
title: "DeepPanoContext: Panoramic 3D Scene Understanding with Holistic Scene Context Graph and Relation-based Optimization"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- admin
- Zhaopeng Cui
- Cai Chen
- Shuaicheng Liu
- Bing Zeng
- Hujun Bao
- Yinda Zhang

# # Author notes (optional)
# author_notes:
# - "Equal contribution"
# - "Equal contribution"
# - "Equal contribution"

date: "2021-08-16T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: International Conference on Computer Vision
publication_short: ICCV 2021

abstract: ""

# Summary. An optional shortened abstract.
summary: We propose a novel method for panoramic 3D scene understanding which recovers the 3D room layout and the shape, pose, position, and semantic category for each object from a single full-view panorama image.

tags:
- Deep Learning
- 3D Reconstruction
- 3D Detection
- 3D Scene Understanding
- Panorama

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
links:
- name: arXiv
  url: 'https://arxiv.org/abs/2108.10743'

url_pdf: ''
url_code: 'https://github.com/chengzhag/DeepPanoContext'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: 'https://www.youtube.com/watch?v=mO1EtUHnX4w'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: '3D scene understanding results'
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


## [<div class="publication-header">ICCV 2021 Oral</div>](http://iccv2021.thecvf.com/home)

<div class="publication-header">
  <a href="https://chengzhag.github.io/" target="_blank">Cheng Zhang</a>
  <sup>1</sup>
  &nbsp; &nbsp;
  <a href="https://zhpcui.github.io/" target="_blank">Zhaopeng Cui</a>
  <sup>2</sup>
  &nbsp; &nbsp;
  <a href="https://github.com/MurrayC7" target="_blank">Cai Chen</a>
  <sup>1</sup>
  &nbsp; &nbsp;
  <a href="http://www.liushuaicheng.org/" target="_blank">Shuaicheng Liu</a>
  <sup>1</sup>
  &nbsp; &nbsp;
  <a href="https://scholar.google.com/citations?user=4y0QncgAAAAJ&hl=en" target="_blank">Bing Zeng</a>
  <sup>1</sup>
  &nbsp; &nbsp;
  <a href="http://www.cad.zju.edu.cn/home/bao/" target="_blank">Hujun Bao</a>
  <sup>2</sup>
  &nbsp; &nbsp;
  <a href="https://www.zhangyinda.com/" target="_blank">Yinda Zhang</a>
  <sup>3</sup>
</div>

<div class="publication-header">
  <sup>1</sup>
  <a href="https://en.uestc.edu.cn/" target="_blank">University of Electronic Science and Technology of China</a> 
  <!-- &nbsp; &nbsp; -->
  <br />
  <sup>2</sup>
  <a href="http://www.cad.zju.edu.cn/english.html" target="_blank">State Key Lab of CAD & CG, Zhejiang University</a> 
  &nbsp; &nbsp;
  <sup>3</sup>
  <a href="https://www.ai.google/" target="_blank">Google</a>
</div>

{{< figure width=90% src="teaser.png" >}}

---
## Abstract
Panorama images have a much larger field-of-view thus naturally encode enriched scene context information compared to standard perspective images, which however is not well exploited in the previous scene understanding methods. 
In this paper, we propose a novel method for panoramic 3D scene understanding which recovers the 3D room layout and the shape, pose, position, and semantic category for each object from a single full-view panorama image. 
In order to fully utilize the rich context information, we design a novel graph neural network based context model to predict the relationship among objects and room layout, and a differentiable relationship-based optimization module to optimize object arrangement with well-designed objective functions on-the-fly. 
Realizing the existing data are either with incomplete ground truth or overly-simplified scene, we present a new synthetic dataset with good diversity in room layout and furniture placement, and realistic image quality for total panoramic 3D scene understanding. 
Experiments demonstrate that our method outperforms existing methods on panoramic scene understanding in terms of both geometry accuracy and object arrangement.

---
## Video

{{< youtube mO1EtUHnX4w >}}

---
## Paper

<center>
  {{< gallery album="pages" >}}
</center>

<center>
  <a href="#" class="btn btn-outline-primary js-cite-modal" data-filename="cite.bib">
  Cite
  </a>
  <a href="https://github.com/chengzhag/DeepPanoContext" class="btn btn-outline-primary" target="_blank">
  Code
  </a>
  <a href="https://www.youtube.com/watch?v=mO1EtUHnX4w" class="btn btn-outline-primary" target="_blank">
  YouTube
  </a>
  <a href="https://www.bilibili.com/video/BV1JU4y1w7Yu/" class="btn btn-outline-primary" target="_blank">
  bilibili
  </a>
  <a href="https://arxiv.org/abs/2108.10743" class="btn btn-outline-primary" target="_blank">
  arXiv (Supp included)
  </a> 
  <a href="https://arxiv.org/pdf/2108.10743" class="btn btn-outline-primary" target="_blank">
  Paper
  </a>
</center>

---
## Pipeline

<figure>
  <div class="d-flex justify-content-center">
    <div class="w-100">
        <img alt="Our proposed pipeline. We first do a bottom-up initialization with several SoTA methods and provide various features, including geometric, semantic, and appearance features of objects and layout. These are then fed into our proposed RGCN network to refine the initial object pose and estimate the relation among objects and layout. A relation optimization is adopted afterward to further adjust the 3d object arrangement to align with the 2D observation, conform with the predicted relation, and resolve physical collision." srcset="
               pipeline_anim.gif" src="pipeline_anim.gif" width="90%" loading="lazy" data-zoomable="" class="medium-zoom-image"></div>
  </div>
  <figcaption>
      Our proposed pipeline. We first do a bottom-up initialization with several SoTA methods and provide various features, including geometric, semantic, and appearance features of objects and layout. These are then fed into our proposed RGCN network to refine the initial object pose and estimate the relation among objects and layout. A relation optimization is adopted afterward to further adjust the 3d object arrangement to align with the 2D observation, conform with the predicted relation, and resolve physical collision.
  </figcaption>
</figure>

We first extract the whole-room layout under Manhattan World assumption and the initial object estimates including locations, sizes, poses, semantic categories, and latent shape codes. 
These, along with extracted features, are then fed into the Relation-based Graph Convolutional Network (RGCN) for refinement and to estimate relations among objects and layout simultaneously.
Then, a differentiable Relation Optimization (RO) based on physical violation, observation, and relation is proposed to resolve collisions and adjust object poses.
Finally, the 3D shape is recovered by feeding the latent shape code into Local Implicit Deep Function (LDIF), and combined with object pose and room layout to achieve total scene understanding. 

---
## Interactive Results

<!-- model-viewer css -->
<link rel="stylesheet" href="model-viewer.css">

<!-- Import the component -->
<script type="module" src="https://unpkg.com/@google/model-viewer/dist/model-viewer.min.js"></script>

<center>
  <div class='container'>
    <div class='row' >
      <div class='column'>
        <p class='header'>Input</p>
      </div>
      <div class='column'>
        <p class='header'>Detection and Layout</p>
      </div>
      <div class='column'>
        <p class='header'>Reconstruction</p>
      </div>
    </div>
    <div class='row' >
      <div class='column'>
        <div id="card">
          {{< figure class="pano" src="input/input-Beechwood_1_int-00094-rgb.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          {{< figure class="pano" src="det3d/Ours-Beechwood_1_int-00094-det3d.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          <model-viewer src="recon/Ours-Beechwood_1_int-00094-rgb.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="629.2deg 46.87deg 9m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
    </div>
    <div class='row' >
      <div class='column'>
        <div id="card">
          {{< figure class="pano" src="input/input-Merom_1_int-00086-rgb.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          {{< figure class="pano" src="det3d/Ours-Merom_1_int-00086-det3d.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          <model-viewer src="recon/Ours-Merom_1_int-00086-rgb.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="540.6deg 40.78deg 11m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
    </div>
    <div class='row' >
      <div class='column'>
        <div id="card">
          {{< figure class="pano" src="input/input-Beechwood_1_int-00089-rgb.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          {{< figure class="pano" src="det3d/Ours-Beechwood_1_int-00089-det3d.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          <model-viewer src="recon/Ours-Beechwood_1_int-00089-rgb.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="540.6deg 40.78deg 9m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
    </div>
    <div class='row' >
      <div class='column'>
        <div id="card">
          {{< figure class="pano" src="input/input-Merom_1_int-00070-rgb.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          {{< figure class="pano" src="det3d/Ours-Merom_1_int-00070-det3d.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          <model-viewer src="recon/Ours-Merom_1_int-00070-rgb.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="809.2deg 39.67deg 9m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
    </div>
    <div class='row' >
      <div class='column'>
        <div id="card">
          {{< figure class="pano" src="input/input-Beechwood_1_int-00069-rgb.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          {{< figure class="pano" src="det3d/Ours-Beechwood_1_int-00069-det3d.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          <model-viewer src="recon/Ours-Beechwood_1_int-00069-rgb.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="540.6deg 40.78deg 9m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
    </div>
  </div>
</center>

---
## Results
{{< figure width=90% src="results.png" caption="Qualitative comparison on 3D object detection and scene reconstruction. We compare object detection and compare scene reconstruction results with Total3D-Pers and Im3D-Pers in both bird's eye view and panorama format." >}}


