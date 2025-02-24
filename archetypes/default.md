---
title: "{{ replace (path.Base (path.Dir .File.Dir)) "-" " " | title }}"
summary: ""
tags: ["{{ path.Base .File.Dir }}"]
date: "{{ .Date }}"
---
