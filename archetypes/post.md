---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: false
slug: "{{ .Name | urlize }}"
# Add Cloudinary image slug without base url
# e.g v1548709265/mood/some_image.jpg, not https://res.cloudinary.com/your_cloud_name/image/upload/v1548709265/mood/some_image.jpg
# If self-hosting image content, make sure you remove `image: ""` from the frontmatter.
image: ""
# Image alt will display below image in grid view
image_alt: ""
# Accepted values: portrait, landscape, wide, square
image_ratio: ""
# Replace example tags below with your own or remove if not required
tags:
- Abstract
- Illustration
- BW
# Must not change
layout: lightbox
---