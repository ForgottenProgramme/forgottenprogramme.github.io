{{- if in .File.Dir "daily" -}}
---
title: "{{ .Date | time.Format "Monday, 2 January 2006" }}"
date: {{ .Date }}
draft: true
---

Just write. It does not have to be good.
{{- else -}}
---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
description: ""   # one line: shown under the title in lists and in link previews
tags: []          # e.g. ["life", "books"] or ["work", "open-source"]
---

Write here.

<!--more-->
{{- end }}
