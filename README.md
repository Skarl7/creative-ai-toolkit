# Creative AI Toolkit

> AI-powered tools for filmmakers, content creators, and digital storytellers

[![OpenAI](https://img.shields.io/badge/OpenAI-412991?logo=openai&logoColor=white)](https://openai.com)
[![Whisper](https://img.shields.io/badge/Whisper-1C3C3C?logo=openai&logoColor=white)](https://openai.com/whisper)
[![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white)](https://nodejs.org)
[![n8n](https://img.shields.io/badge/n8n-EA4B71?logo=n8n&logoColor=white)](https://n8n.io)

**Built by** [Skarl7](https://github.com/Skarl7) | [AdnexAI](https://www.adnexai.co.uk)

---

## Overview

Creative AI Toolkit is a collection of AI-powered content creation tools designed for independent filmmakers, YouTubers, and content creators. It automates the entire content pipeline from script to published video.

## Tools Included

| Tool | Description | Tech Stack |
|------|-------------|------------|
| Script-to-Storyboard | Generate visual storyboards from scripts | OpenAI GPT-4o, DALL-E 3 |
| Auto Voiceover | Text-to-speech voiceover generation | ElevenLabs API, OpenAI TTS |
| YouTube Shorts Engine | End-to-end Shorts creation pipeline | n8n, OpenAI, YouTube API |
| Subtitle Generator | AI-powered subtitle and caption creation | OpenAI Whisper |
| Content Repurposer | Transform long-form to short-form content | OpenAI GPT-4o |
| Hashtag Optimiser | AI-generated SEO hashtags | OpenAI + trending data |

## YouTube Shorts Engine

### Pipeline

```
[Script] → [AI Analysis] → [Voiceover] → [Visual Assembly] → [Upload]
    ↓           ↓              ↓              ↓                 ↓
 OpenAI      Scene list    ElevenLabs    FFmpeg +         YouTube API
 Writer     extraction     TTS engine   templates        auto-publish
```

### Features

- **One-click generation** — Input a topic, get a complete Short
- **Custom voice selection** — Choose from professional AI voices
- **Brand templates** — Consistent intro/outro animations
- **Auto captions** — Built-in Whisper subtitle generation
- **Cross-platform export** — TikTok, Reels, and Shorts formats

## Getting Started

### Prerequisites

- Node.js 18+
- OpenAI API key
- ElevenLabs API key (for voiceover)
- YouTube API credentials
- FFmpeg installed

### Installation

```bash
git clone https://github.com/Skarl7/creative-ai-toolkit
cd creative-ai-toolkit
npm install
```

### Configuration

```bash
cp .env.example .env
OPENAI_API_KEY=sk-...
ELEVENLABS_API_KEY=...
YOUTUBE_CLIENT_ID=...
YOUTUBE_CLIENT_SECRET=...
OUTPUT_DIR=./output/
```

### Usage Examples

#### Generate a Short

```bash
node scripts/generate-short.js --topic "5 AI tools for lawyers" --voice "adam" --duration 45
```

#### Create Storyboard

```bash
node scripts/storyboard.js --script ./scripts/legal-intro.txt --scenes 6
```

#### Generate Subtitles

```bash
node scripts/subtitles.js --video ./draft.mp4 --language en
```

## File Structure

```
creative-ai-toolkit/
├── scripts/
│   ├── generate-short.js
│   ├── storyboard.js
│   ├── subtitles.js
│   └── voiceover.js
├── templates/
│   ├── intro-animation/
│   └── outro-animation/
├── workflows/
│   └── shorts-pipeline.json
├── output/
└── docs/
    └── workflow-diagram.md
```

## Workflow Diagram

```
input → OpenAI → ElevenLabs → FFmpeg → YouTube
 script  script    voiceover   render    upload
         outline   engine      + edit
         + scenes  + BGM
```

## Roadmap

- [x] YouTube Shorts pipeline (end-to-end)
- [x] Voiceover generation
- [x] Auto subtitle creation
- [ ] Storyboard visual generation (DALL-E 3)
- [ ] Batch video processing
- [ ] Multi-language support
- [ ] Content calendar integration

## License

Apache 2.0

---
*Part of the AdnexAI creative ecosystem — www.adnexai.co.uk*
