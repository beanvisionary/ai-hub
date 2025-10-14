# Content Management Guide

## Overview
Jekyll's site uses a data-driven content management system that makes it easy to update content without touching HTML code.

## Content Structure

### 1. Site Content (Managed via `_data/site_content.yml`)
This file controls all the main content of the homepage:

- **Hero Section**: Title, subtitle, and call-to-action button
- **Blog Section**: Section title and configuration
- **Logo**: Site logo configuration  
- **Footer**: Copyright and links

### 2. AI News Articles (Managed via `_ai_news/` collection)
Each article is a separate Markdown file in the `_ai_news/` folder with structured front matter.

## How to Add New Content

### Adding a New AI News Article
1. Create a new `.md` file in `_ai_news/` folder
2. Use this template:

```markdown
---
title: "The Article Title"
date: 2025-10-13
source: "Source Name"
source_url: "https://example.com/article"
category: "ai-category"
tags: ["tag1", "tag2", "tag3"]
image: "/assets/images/your-image.png"
image_alt: "Description of image"
excerpt: "Brief summary of the article..."
featured: true
---

Full article content goes here in Markdown format.
```

### Updating Homepage Content
Edit `_data/site_content.yml`:

```yaml
# Update hero section
hero:
  title: "New Title"
  subtitle: "New subtitle"

# Add new features
features:
  - title: "New Feature"
    description: "Description of feature"
    icon: "🔧"
```

## Content Types

### Categories for AI News
- `ai-hardware` - Hardware and chip developments
- `ai-transformation` - Business transformation stories
- `ai-development` - Development tools and platforms
- `ai-research` - Research breakthroughs
- `ai-policy` - Policy and regulation news

### Tags
Use descriptive tags like: `["OpenAI", "machine-learning", "enterprise"]`

## Images
- Place images in `assets/images/`
- Use descriptive filenames
- Always include `image_alt` for accessibility

## Featured Articles
Set `featured: true` to show articles prominently on the homepage.

## Testing Changes
After making changes:
1. Run `bundle exec jekyll build` to test
2. Check `_site/` folder for generated files
3. Run `bundle exec jekyll serve` to preview locally

## Best Practices
- Keep article titles concise but descriptive
- Write compelling excerpts (1-2 sentences)
- Use high-quality images with proper alt text
- Keep content up-to-date and accurate
- Use consistent categories and meaningful tags