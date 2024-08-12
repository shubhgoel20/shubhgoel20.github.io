---
title: "A Hardware Accelerator for Contour Tracing in Real-Time Imaging"
authors:
- Sonal Gupta
- admin
- Ayush Kumar
- Subrat Kar
date: "2024-07-29"
doi: "https://doi.org/10.1109/JSEN.2024.3432129"

# Schedule page publish date (NOT publication's date).
#publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Sensors Journal"
publication_short: ""

abstract: Contour tracing is a critical technique in image analysis and computer vision, with applications in medical imaging, big data analytics, machine learning, and robotics. We introduce a novel hardware accelerator based on the Adapted and Segmented (AnS) Vertex Following and Run-Data-Based-Following families of fast contour tracing algorithms implemented on the Zynq-7000 FPGA platform. Our algorithmic implementation utilizing a mesh-interconnected multiprocessor architecture is at least 55 times faster than the existing implementations. With input-output overheads, it is up to 12.5 times faster. Our hardware accelerator for contour tracing is benchmarked on mesh-interconnected hardware, all three families of contour tracing algorithms, and a random image from the Imagenet database. Our implementation is, thus, faster for FPGA, ASIC, GPU, and supercomputer hardware in comparison to the CPU-GPU collaborative approach and offers a better solution for those systems where the input-output overheads can be minimized, like parallel processing arrays and mesh-connected sensor networks.

# Summary. An optional shortened abstract.
summary: ""

# tags:
# - Source Themes
featured: true

# links:
# - name: Custom Link
#   url: http://example.org
url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/s9CC2SKySJM)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

<!-- {{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/). -->
