# 211-KIC-RSVP Copilot Instructions

## Repository Purpose

This repository contains a simple static web application for generating mascot images for various 211 organizations across California. The tool uses the Google Gemini API to generate custom mascot images based on predefined prompts.

## Project Overview

- **Type**: Static HTML/CSS/JavaScript web application
- **Tech Stack**: 
  - Pure HTML5
  - Tailwind CSS (via CDN)
  - Vanilla JavaScript
  - Google Gemini API for image generation
- **No Build Process**: This is a static site with no build tools or dependencies
- **No Testing Framework**: Currently no automated tests

## File Structure

```
/
├── .github/
│   └── copilot-instructions.md (this file)
├── index.html                   # Main application file
└── README.md                    # Project documentation
```

## Key Features

1. **Mascot Generation**: Generate AI-powered mascot images for 13 different 211 organizations
2. **Interactive UI**: Navigate through mascots using Previous/Next buttons
3. **Custom Prompts**: Edit and customize prompts before generation
4. **Download Functionality**: Save generated images with proper filenames

## Coding Guidelines

### HTML/JavaScript Standards
- Use semantic HTML5 elements
- Keep JavaScript vanilla (no frameworks)
- Use ES6+ features (const/let, arrow functions, async/await)
- Follow existing code style and indentation (4 spaces)
- Keep inline styles minimal, prefer Tailwind utility classes

### API Integration
- API calls use the Gemini API endpoint stored in `apiUrl` constant
- API key is expected to be empty and injected by the environment
- Handle API errors gracefully with user-friendly messages

### Code Organization
- Keep all code in `index.html` for simplicity
- Use clear function names with JSDoc-style comments
- Separate concerns: DOM manipulation, API calls, event handlers

### UI/UX Principles
- Maintain dark theme (gray-800/gray-900 backgrounds)
- Use Tailwind's color palette for consistency
- Provide visual feedback for loading states
- Display clear error messages to users

## Making Changes

### When Modifying HTML/CSS
- Preserve the existing Tailwind CSS classes and color scheme
- Test responsive behavior at different screen sizes
- Ensure accessibility features remain intact

### When Modifying JavaScript
- Maintain the existing function structure
- Keep async/await pattern for API calls
- Update JSDoc comments if function signatures change
- Test error handling paths

### When Adding Features
- Keep the single-file structure unless complexity requires separation
- Use the existing utility functions and patterns
- Update this instructions file if adding new conventions

## Testing Approach

Since there's no automated testing framework:
- Manually test all changes in a browser
- Verify the mascot navigation (Previous/Next buttons)
- Test image generation with sample prompts
- Check error handling with invalid API scenarios
- Test download functionality with generated images

## Deployment

This is a static site that can be:
- Served directly from the filesystem
- Hosted on any static hosting service (GitHub Pages, Netlify, etc.)
- No build or deployment scripts required

## Common Tasks

### Adding a New Mascot
1. Add new entry to the `all211s` array in the JavaScript section
2. Include: id, name, mascotName, and prompt properties
3. Follow existing prompt format (vector art, headset, clean white background)

### Modifying UI Styles
1. Use Tailwind utility classes when possible
2. Add custom styles to the `<style>` section if needed
3. Keep consistent with existing color scheme and spacing

### Updating API Configuration
1. Modify the `apiKey`, `genModel`, or `apiUrl` constants
2. Test with valid API credentials
3. Ensure error handling covers new API response formats

## Important Notes

- **API Key**: The application expects an API key to be provided externally
- **Rate Limiting**: Free tier API has strict rate limits (60-second cooldown)
- **Image Format**: Generated images are returned as base64-encoded PNG data
- **Filename Convention**: Download filenames use lowercase with underscores (e.g., `the_hollywood_star.png`)

## Contribution Guidelines

- Keep changes minimal and focused
- Preserve existing functionality unless fixing bugs
- Document any new features or significant changes
- Test manually before submitting changes
- Update this instructions file if adding new patterns or conventions
