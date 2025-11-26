# YouTube Video SEO Analyzer

A lightweight, web-based tool designed to help creators improve their video performance through data-driven SEO analysis. This application connects to the YouTube Data API to gather metadata and engagement metrics, calculates a reproducible SEO score, and provides actionable optimization recommendations.

https://ryanmend.github.io/Youtube-SEO-Analyzer/

## Features

*   **Real-time Data Collection:** Fetches live video statistics (views, likes, comments) and metadata (tags, description, title) using the YouTube Data API v3.
*   **SEO Scoring Engine:** A transparent algorithm that scores videos from 0-100 based on keyword placement, tag usage, and engagement ratios.
*   **Interactive Dashboard:** Compare multiple videos side-by-side, sort by score, and view performance insights.
*   **Optimization Recommendations:** Tailored advice on how to improve specific aspects of a video (e.g., "Add your keyword to the title," "Increase tag count").
*   **Demo Mode:** Includes a "Load Sample Data" feature to demonstrate the dashboard functionality without needing an immediate API key.

## Technologies

*   **HTML5 & Vanilla JavaScript:** No build steps, bundlers, or frameworks (React/Vue/Angular) required.
*   **Tailwind CSS:** Used via CDN for rapid, responsive styling.
*   **YouTube Data API v3:** For retrieving public video data.

## Getting Started

### Prerequisites

*   A modern web browser (Chrome, Firefox, Safari, Edge).
*   A text editor (if you wish to modify the code).

### Installation

1.  Download the `index.html` file.

That's it! There is no `npm install` or build process.

### Running the App

Double-click `index.html` to open it in your browser.

Alternatively, you can serve it using a simple local server (e.g., Live Server in VS Code) to avoid potential CORS issues depending on strict browser security settings, though the file is designed to work directly.

### Usage Guide

1.  **Get an API Key:**
    *   Go to the [Google Cloud Console](https://console.cloud.google.com/).
    *   Create a new project and enable the YouTube Data API v3.
    *   Create Credentials (API Key) and copy the key string.

2.  **Analyze a Video:**
    *   Paste your API Key into the Configuration box in the dashboard.
    *   Enter a YouTube Video URL (e.g., `https://www.youtube.com/watch?v=...`).
    *   Enter a Target Keyword (e.g., `"cooking tutorial"`). This is the term you want to rank for; the analyzer checks if your video is optimized for this specific phrase.
    *   Click "Analyze Video".

3.  **Review Results:**
    *   The video will appear in the list with a color-coded score.
    *   Expand the card to see specific warnings and recommendations.
    *   Check the "Comparative Insights" sidebar to see how the video stacks up against others in the session.

## Scoring Methodology

The SEO Score (0-100) is calculated using a weighted sum of the following criteria:

| Criteria             | Weight | Description                                    |
| -------------------- | ------ | ---------------------------------------------- |
| Keyword in Title    | 25 pts | Checks if the target keyword appears exactly in the video title. |
| Engagement Rate      | 25 pts | Checks if the Like-to-View ratio is healthy (> 3.5%). |
| Keyword in Description | 15 pts | Checks if the keyword appears in the video description. |
| Recency              | 15 pts | Checks if the video was published within the last 365 days. |
| Tag Utilization      | 10 pts | Checks if the video uses at least 5 tags.       |
| Description Depth    | 10 pts | Checks if the description is longer than 250 characters. |

## License

This project is built for educational purposes. Data provided by YouTube Data API v3.
