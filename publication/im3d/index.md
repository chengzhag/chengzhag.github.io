---
title: "Holistic 3D Scene Understanding from a Single Image with Implicit Representation"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- admin
- Zhaopeng Cui
- Yinda Zhang
- Bing Zeng
- Marc Pollefeys
- Shuaicheng Liu

# Author notes (optional)
author_notes:
- "Equal contribution"
- "Equal contribution"
- "Equal contribution"

date: "2021-03-11T00:00:00Z"
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
publication_short: CVPR 2021

abstract: ""

# Summary. An optional shortened abstract.
summary: We present a new pipeline which takes a single image as input, estimates layout and object poses, then reconstructs the scene with Signed Distance Function (SDF) representation.

tags:
- Deep Learning
- 3D Reconstruction
- 3D Detection
- 3D Scene Understanding
- Layout Estimation

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
links:
- name: arXiv
  url: 'https://arxiv.org/abs/2103.06422'

url_pdf: ''
url_code: 'https://github.com/pidan1231239/Implicit3DUnderstanding'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: 'https://www.youtube.com/watch?v=Kg0du7mFu60'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Scene reconstruction comparison'
  focal_point: Smart
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

## [<div class="publication-header">CVPR 2021</div>](http://cvpr2021.thecvf.com/)

<div class="publication-header">
  <a href="https://chengzhag.github.io/" target="_blank">Cheng Zhang</a>
  <sup>2</sup>*
  &nbsp; &nbsp;
  <a href="https://zhpcui.github.io/" target="_blank">Zhaopeng Cui</a>
  <sup>1</sup>*
  &nbsp; &nbsp;
  <a href="https://www.zhangyinda.com/" target="_blank">Yinda Zhang</a>
  <sup>3</sup>*
  &nbsp; &nbsp;
  <a href="https://scholar.google.com/citations?user=4y0QncgAAAAJ&hl=en" target="_blank">Bing Zeng</a>
  <sup>2</sup>
  &nbsp; &nbsp;
  <a href="https://people.inf.ethz.ch/pomarc/" target="_blank">Marc Pollefeys</a>
  <sup>4</sup>
  &nbsp; &nbsp;
  <a href="http://www.liushuaicheng.org/" target="_blank">Shuaicheng Liu</a>
  <sup>2</sup>
</div>

<div class="publication-header">
  <sup>1</sup>
  <a href="http://www.cad.zju.edu.cn/english.html" target="_blank">State Key Lab of CAD & CG, Zhejiang University</a> 
  <!-- &nbsp; &nbsp; -->
  <br />
  <sup>2</sup>
  <a href="https://en.uestc.edu.cn/" target="_blank">University of Electronic Science and Technology of China</a> 
  &nbsp; &nbsp;
  <sup>3</sup>
  <a href="https://www.ai.google/" target="_blank">Google</a> 
  &nbsp; &nbsp;
  <sup>4</sup>
  <a href="https://ethz.ch/en.html" target="_blank">ETH Zurich</a> 
</div>

{{< figure src="featured.png" >}}

---
## Abstract
We present a new pipeline for holistic 3D scene understanding from a single image, which could predict object shape, object pose, and scene layout. As it is a highly ill-posed problem, existing methods usually suffer from inaccurate estimation of both shapes and layout especially for the cluttered scene due to the heavy occlusion between objects. We propose to utilize the latest deep implicit representation to solve this challenge. We not only propose an image-based local structured implicit network to improve the object shape estimation, but also refine 3D object pose and scene layout via a novel implicit scene graph neural network that exploits the implicit local object features. A novel physical violation loss is also proposed to avoid incorrect context between objects. Extensive experiments demonstrate that our method outperforms the state-of-the-art methods in terms of object shape, scene layout estimation, and 3D object detection.

<!-- ## 3D Scene Understanding 
Given a single color image,
- Estimate the room layout, including object categories and poses in 3D space
- Reconstruct mesh of individual object -->

---
## Video

{{< youtube Kg0du7mFu60 >}}

---
## Paper
<!-- ![page1](02192_页面_01.png)![page3](02192_页面_03.png)![page5](02192_页面_05.png)![page7](02192_页面_07.png) -->

<center>
  {{< gallery album="pages" >}}
</center>

<center>
  <!-- {{< cta cta_text="arXiv" cta_link="https://arxiv.org/abs/2103.06422" cta_new_tab="false" >}} -->

  <!-- <a href="https://arxiv.org/abs/2103.06422" class="btn btn-primary px-3 py-3">Paper</a> -->

  <a href="#" class="btn btn-outline-primary js-cite-modal" data-filename="cite.bib">
  Cite
  </a>
  <a href="https://github.com/pidan1231239/Implicit3DUnderstanding" class="btn btn-outline-primary" target="_blank">
  Code
  </a>
  <a href="https://www.youtube.com/watch?v=Kg0du7mFu60" class="btn btn-outline-primary" target="_blank">
  YouTube
  </a>
  <a href="https://www.bilibili.com/video/BV1By4y1g7c5/" class="btn btn-outline-primary" target="_blank">
  bilibili
  </a>
  <a href="https://arxiv.org/abs/2103.06422" class="btn btn-outline-primary" target="_blank">
  arXiv
  </a> 
  <a href="https://arxiv.org/pdf/2103.06422" class="btn btn-outline-primary" target="_blank">
  Paper
  </a>
</center>

<!-- <center>
  <a href="https://arxiv.org/abs/2103.06422">[arXiv]</a> 
  &nbsp; &nbsp;
  <a href="https://arxiv.org/pdf/2103.06422">[Paper]</a> 
  &nbsp; &nbsp;
  <a href="02192-supp.pdf">[Supp]</a> 
  &nbsp; &nbsp;
  <a href="https://github.com/pidan1231239/Implicit3DUnderstanding">[GitHub]</a>
</center> -->

---
## Motivations
- Implicit representation like Signed Distance Function (SDF) can be used to detect collision and propagate gradients
- And together with structured representation (LDIF), the shapes can be learned better and more shape priors can be provided for relationship understanding
- Graph Convolutional Network (GCN) is proven to be good at resolving context information in the task of scene graph generation

---
## Pipeline
{{< figure src="pipeline.png" caption="Our proposed pipeline. We initialize the layout estimation and 3D object poses with LEN and ODN from prior work, then refine them with Scene Graph Convolutional Network (SGCN). We utilize a Local Implicit Embedding Network (LIEN) to encode latent code for LDIF decoder and to extract implicit features for SGCN. With the help of LDIF and marching cube algorithm, object meshes are extracted then rotated, scaled, and put into places to construct the scene." >}}

The proposed system consists of two stages, i.e., the initial estimation stage, and the refinement stage. 
In the initial estimation stage, a 2D detector is first adopted to extract the 2D bounding box from the input image, followed by an Object Detection Network (ODN) to recover the object poses as 3D bounding boxes and a new Local Implicit Embedding Network (LIEN) to extract the implicit local shape information from the image directly, which can further be decoded to infer 3D geometry.
The input image is also fed into a Layout Estimation Network (LEN) to produce a 3D layout bounding box and relative camera pose.
In the refinement stage, a novel Scene Graph Convolutional Network (SGCN) is designed to refine the initial predictions via the scene context information.

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
        <p class='header'>Total3D</p>
      </div>
      <div class='column'>
        <p class='header'>Ours</p>
      </div>
    </div>
    <div class='row' >
      <div class='column'>
        <div id="card">
          {{< figure class="input" src="input/002435.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          <model-viewer src="total3d/2435_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2.7m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
      <div class ='column'>
        <div id="card">
          <model-viewer src="im3d/2435_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2.7m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
    </div>
    <div class='row' >
      <div class='column'>
        <div id="card">
          {{< figure class="input" src="input/000724.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          <model-viewer src="total3d/724_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
      <div class ='column'>
        <div id="card">
          <model-viewer src="im3d/724_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
    </div>
    <div class='row' >
      <div class='column'>
        <div id="card">
          {{< figure class="input" src="input/000276.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          <model-viewer src="total3d/276_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2.7m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
      <div class ='column'>
        <div id="card">
          <model-viewer src="im3d/276_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2.7m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
    </div>
    <div class='row' >
      <div class='column'>
        <div id="card">
          {{< figure class="input" src="input/001140.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          <model-viewer src="total3d/1140_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2.7m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
      <div class ='column'>
        <div id="card">
          <model-viewer src="im3d/1140_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2.7m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
    </div>
    <div class='row' >
      <div class='column'>
        <div id="card">
          {{< figure class="input" src="input/000765.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          <model-viewer src="total3d/765_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
      <div class ='column'>
        <div id="card">
          <model-viewer src="im3d/765_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
    </div>
    <div class='row' >
      <div class='column'>
        <div id="card">
          {{< figure class="input" src="input/001149.jpg" >}}
        </div>
      </div>
      <div class='column'>
        <div id="card">
          <model-viewer src="total3d/1149_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
      <div class ='column'>
        <div id="card">
          <model-viewer src="im3d/1149_mesh.glb" interaction-prompt="when-focused" camera-controls exposure="0.72" shadow-intensity="2.7" shadow-softness="0.84" camera-target="2m -0.5m 0.1m" min-camera-orbit="auto auto auto" max-camera-orbit="auto auto 11.89m" camera-orbit="270deg 50deg 8m" field-of-view="30deg">
          </model-viewer> 
        </div>
      </div>
    </div>
  </div>
</center>


---
## Results
{{< figure src="results.png" caption="Qualitative comparison on object detection and scene reconstruction. We compare object detection results with Total3D and ground truth in both oblique view and camera view. The results show that our method gives more accurate bounding box estimation and with less intersection. We compare scene reconstruction results with Total3D in camera view and observe more reasonable object poses." >}}


