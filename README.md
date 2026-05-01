# Automated Web Data Extraction and Download Tool

## Overview
I built this tool to automate pulling video and file content from complex websites that don’t load everything at once. The goal was to replace a very manual process with something reliable that could run on its own.

## What it does
- Navigates web pages automatically using Selenium (clicking, typing, downloading)
- Handles dynamic content like scrolling, delayed loading, and changing layouts
- Uses a machine learning-based approach to detect and interact with overlay buttons that are not easily accessible through standard automation
- Downloads and organizes video files, including selecting the best available quality
- Processes 500+ files and structures them into clean, usable folders
- Supports downloads from multiple sources, including S3-hosted content

## Key Challenges Solved
- **Dynamic pages:** Many elements only appear after scrolling or waiting, so I built logic to detect and handle that
- **Overlay elements:** Some buttons were hidden or blocked by overlays, so I implemented a machine learning-based method to reliably identify and interact with them
- **Changing layouts:** Buttons and elements moved or changed, so the system adapts instead of relying on fixed positions
- **Reliability:** Added retries, validation, and error handling so the process can run without breaking
- **File management:** Automatically cleans filenames, avoids duplicates, and keeps everything organized

## Tech Stack
- **Python**
- **Selenium WebDriver** for browser automation
- **Requests / urllib** for downloading files
- **PyAutoGUI** for screen-based interactions when needed
- **PyPDF2 / pdfkit** for handling PDF files
- **OpenAI API** for text processing
- **JSON / Regex** for parsing and cleaning data

## Impact
- Reduced manual work by over 80%
- Turned a repetitive multi-day task into an automated process that can run unattended
- Made large amounts of unstructured content easier to access and analyze
