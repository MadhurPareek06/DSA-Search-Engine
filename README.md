# DSA Search Engine

A full-stack Data Structures & Algorithms (DSA) problem search engine powered by automated web scraping, text preprocessing, and a TF-IDF vector space ranking backend. Built to help programmers rapidly discover relevant coding problems by topic, algorithm, or problem description.

## Features

- **TF-IDF Relevance Ranking:** Implements Term Frequency–Inverse Document Frequency (`natural`) with cosine similarity scoring and title-weight boosting to surface the most relevant problems first.
- **NLP Text Preprocessing:** Tokenizes problem titles and descriptions while filtering out noise via custom stopword removal (`stopword`).
- **Automated Data Pipeline:** Includes headless browser scraping scripts (`Puppeteer`) and corpus merging utilities (`utils/merge.js`) to build and update the structured problem dataset (`corpus/all_problems.json`).
- **Fast Search Interface:** Lightweight, responsive frontend (`HTML5`, `CSS3`, `Vanilla JS`) served over a RESTful `Node.js` and `Express` backend.

## Tech Stack

- **Backend:** Node.js, Express.js
- **Search & NLP:** `natural` (TF-IDF), `stopword`, Cosine Similarity
- **Web Scraping & Data Pipeline:** Puppeteer
- **Frontend:** HTML5, CSS3, Vanilla JavaScript

## Getting Started

### Prerequisites
- Node.js (v18 or higher)
- npm

### Installation & Local Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/MadhurPareek06/DSA-Search-Engine.git
   cd DSA-Search-Engine
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the server:**
   ```bash
   npm start
   ```
   Open [http://localhost:3000](http://localhost:3000) in your browser to start searching.

### Optional: Rebuilding the Problem Corpus
- Run `npm run scrape` to collect problem data via Puppeteer.
- Run `npm run merge` to consolidate scraped files into `corpus/all_problems.json`.
