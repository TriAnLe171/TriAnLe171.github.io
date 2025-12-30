---
layout: page
title: "Research"
permalink: /research/
---

## Research Overview

My work centers on **multimodal and multilingual NLP** in **online communities**. I’m especially interested in:

- **Multimodal meaning**: how text overlays + images jointly convey intent, humor, sarcasm, and emotion
- **Noisy social media language**: short, informal, context-dependent, often ambiguous
- **Retrieval & recommendation**: representation learning that supports user intent + context
- **Code-switching**: Vietnamese–English mixed language understanding

---

## Current Project: MemeMatch

**Goal:** build a scalable, reusable resource for studying and retrieving memes using a **dual-context representation**.

**Core ideas**
- Separate meme meaning into:
  - **Local**: OCR text + title (what the user says)
  - **Global**: template semantics (what the image depicts)
- Enrich each view with:
  - sentiment/emotion vectors
  - topics
  - usage-intent labels
- Support **text search**, **image search**, and **intent-aware retrieval**

**Why it matters**
Memes are a key unit of communication online, but their meaning is inherently multimodal and culturally contextual. Dual-context modeling helps preserve both message and form.

---

## Methods I Use

- OCR pipelines (overlay text extraction + template artifact filtering)
- Vision-language captioning for template semantics (mask text then caption)
- Transformer-based emotion/sentiment + topic modeling
- Embedding-based retrieval (cosine similarity) + lightweight query parsing

---

## Collaboration

If you’re working on multimodal NLP, social media analysis, code-switching, or retrieval systems, feel free to reach out.
