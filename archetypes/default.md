---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
author: "Fletcher Kelly"
draft: true
---

{{- range .Params.authors }}
  {{- with $.Site.GetPage "taxonomyTerm" (printf "authors/%s" (urlize .)) }}
    <figure>
      <img src="{{ .Params.photo }}" alt=""/>
      <figcaption>
        <a href="{{ .Permalink }}">{{ .Params.name }}</a>
      </figcaption>
    </figure>
  {{ end }}
{{ end }}