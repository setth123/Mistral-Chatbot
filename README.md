# Multimodal Chatbot with Mistral, BLIP, BART, and Stable Diffusion
## Project overview
This is an intelligent **multimodal chatbot** that combines state-of-the-art language and vision models to:
- Understand and generate human-like conversation (Mistral)
- Describe images (BLIP)
- Pdf file processing with pdfplumber, summarize long texts ìn file with face/bart-large-cnn
- Generate images from text (Stable Diffusion)

## Model Components

| Model | Role | Source |
|-------|------|--------|
| [Mistral 7B](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.1) | Natural language conversation | Mistral AI |
| [BLIP](https://huggingface.co/Salesforce/blip-image-captioning-base) | Image captioning | Salesforce |
| [facebook/bart-large-cnn](https://huggingface.co/facebook/bart-large-cnn) | Text summarization | Meta AI |
| [Stable Diffusion](https://huggingface.co/runwayml/stable-diffusion-v1-5) | Text-to-image generation | CompVis / Runway |

---

## System Architecture

1. User inputs either text or an image.
2. The system detects the type of request:
   - Text chat → uses Mistral
   - Image → either describe with BLIP or generate new image with Stable Diffusion
3. Response is returned in the chatbot interface.
