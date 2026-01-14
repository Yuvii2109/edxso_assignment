# AI-Powered Upwork Job Tracker

An automated workflow built with **n8n**, **Google Gemini**, and **Airtable** to filter and prioritize freelance job opportunities.

## Features
* **Ingestion:** Simulates fetching job data (Scraper/JSON).
* **AI Analysis:** Uses Google Gemini to read job descriptions and score them based on relevance to my skills (Python, AI, Automation).
* **Database Sync:** Automatically saves high-potential leads to Airtable with a "Priority" tag and "Reasoning."
* **Error Handling:** Auto-converts relative time formats to ISO dates.

## Setup & Installation

### Prerequisites
* [Docker](https://www.docker.com/) (if running n8n locally)
* Airtable Account (Free tier is fine)
* Google Cloud Platform Account (for Gemini API)

### 1. Run n8n with Docker
```bash
docker run -it --rm --name n8n -p 5678:5678 -v ~/.n8n:/home/node/.n8n n8nio/n8n