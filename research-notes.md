---
layout: page
title: "Translational Research"
permalink: /research-notes/
---

Translating methodological research into practical insights for applied social and organizational research.

## About This Page

A collection of translational research notes focused on bridging the gap between methodological research and applied practice.

My goal is to make research methods—particularly in psychometrics and quantitative modeling—more accessible and actionable for real-world applications. There is often a disconnect between methodological advances and how research is actually conducted in practice. At the same time, there is a gap between psychometric theory and its use in applied social and organizational research.

These notes are an attempt to close those gaps by translating technical ideas into practical insights for researchers and practitioners.

While I occasionally draw on examples from published research, the goal is not to critique individual studies or authors. Instead, I aim to highlight common methodological patterns and practices that are widely used, but not always well aligned with underlying statistical principles.

I approach business and social science research as a form of science that should be held to rigorous standards. Throughout my PhD training, I have often observed that statistical methods are learned and applied in a procedural way—where researchers replicate existing practices without fully understanding the underlying assumptions and mathematical foundations.

This issue may partially contribute to broader challenges such as the replication crisis. In many applied domains, errors in design or analysis have tangible consequences. In contrast, in academic research, methodological shortcomings often have less immediate consequences.

As a result, the current incentive structure may not always encourage deep engagement with psychometric and statistical principles.

## Posts

<ul style="list-style:none; padding-left:0; margin-top:20px;">
  {% for post in site.posts %}
    <li style="margin-bottom:28px; border-bottom:1px solid #f1f5f9; padding-bottom:16px;">
      <a href="{{ post.url }}" style="font-size:20px; font-weight:700;">
        {{ post.title }}
      </a>
      <div style="color:#6b7280; font-size:14px;">
        {{ post.date | date: "%B %Y" }}{% if post.tags %} · {{ post.tags | join: " · " }}{% endif %}
      </div>
      <p style="margin-top:6px; max-width:700px;">
        {{ post.excerpt | strip_html | truncate: 180 }}
      </p>
    </li>
  {% endfor %}
</ul>
