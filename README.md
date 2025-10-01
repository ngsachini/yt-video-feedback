# YouTube Video Grade Analyzer

A Node.js application that analyzes YouTube videos using generative AI models to provide educational assessments.

## Features

- Simple web interface to input YouTube video URL and subject
- Uses generative AI models (OpenAI GPT or Google Gemini) for video analysis
- Generates a rubric based on the subject
- Analyzes video content against the rubric
- Provides scores for each rubric item and an overall grade
- Displays results in a clean, tabular format

## Tech Stack

- **Backend**: Node.js with Express
- **Frontend**: EJS templates with HTML/CSS
- **Generative AI Models**: 
  - OpenAI GPT-4o-mini (primary model)
  - Google Gemini 1.5 Flash (alternative model)
- **Other**: Axios for HTTP requests, Dotenv for environment management

## Setup Instructions

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up environment variables:
   - Copy `.env.example` to `.env`
   - Add your API keys:
     ```
     OPENAI_API_KEY=your_openai_api_key_here
     GEMINI_API_KEY=your_gemini_api_key_here
     ```
4. Start the server:
   ```bash

   npm start
   ```
5. Visit `http://localhost:3000` in your browser

## Development

For development with auto-restart:
```bash
npm run dev
```

## How It Works

1. User submits a YouTube video URL and subject
2. The app uses a generative AI model to analyze the video content
3. The AI generates a rubric and grades the video
4. Results are displayed in a table format

## Generative AI Model Configuration

The application supports both OpenAI and Google Gemini generative models:

- If `OPENAI_API_KEY` is provided, it will use OpenAI's GPT-4o-mini for analysis
- If `GEMINI_API_KEY` is provided, it will use Google's Gemini 1.5 Flash for analysis
- If neither is provided, it will return mock data for demonstration

## Example Usage

1. Enter a YouTube URL: `https://www.youtube.com/watch?v=dQw4w9WgXcQ`
2. Enter a subject: `Introduction to AI`
3. Submit the form
4. View the rubric and grades in the results table

## Project Structure

```
yt-grade-analyzer/
├── server.js          # Main server file
├── views/             # EJS templates
│   ├── index.ejs      # Input form
│   └── result.ejs     # Results display
├── public/            # Static assets (CSS, JS, images)
├── .env               # Environment variables
├── package.json       # Project dependencies and scripts
└── README.md          # This file
```