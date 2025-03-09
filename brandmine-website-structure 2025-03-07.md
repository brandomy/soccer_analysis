# Brandmine Website Structure Documentation

## Overview

This document provides a comprehensive overview of the Brandmine Jekyll website structure. Brandmine is a platform designed to showcase consumer brands from BRICS+ countries, with multilingual support for English, Russian, and Chinese.

## File Structure

```
brandmine-site/
├── 404.html                  # Custom 404 error page
├── CNAME                     # Custom domain configuration for GitHub Pages
├── Gemfile                   # Ruby dependencies for Jekyll
├── Gemfile.lock              # Locked versions of dependencies
├── _brands/                  # Custom collection for brand profiles
│   ├── en/                   # English brand profiles
│   ├── ru/                   # Russian brand profiles
│   └── zh/                   # Chinese brand profiles
├── _config.yml               # Jekyll configuration
├── _data/                    # Data files for the site
│   ├── sectors.yml           # Sector definitions
│   └── translations/         # Language translations
│       ├── en.yml            # English translations
│       ├── ru.yml            # Russian translations
│       └── zh.yml            # Chinese translations
├── _includes/                # Reusable HTML components
│   ├── footer.html           # Site footer
│   ├── google-analytics.html # Analytics tracking code
│   ├── header.html           # Site header
│   └── language-selector.html # Language switcher
├── _layouts/                 # Layout templates
│   └── default.html          # Main layout template
├── _posts/                   # Blog posts
│   └── 2025-03-06-welcome-to-jekyll.markdown
├── _site/                    # Generated site (not tracked in version control)
├── about.markdown            # About page
├── assets/                   # Static assets
│   └── css/                  # CSS files
│       └── basic-colors.css  # Color system and component styles
├── index.html                # Root redirect to English version
├── index.markdown            # Default Jekyll index page
├── package-lock.json         # NPM dependencies lock file
├── package.json              # NPM configuration
├── pages/                    # Static pages organized by language
│   ├── en/                   # English pages
│   │   └── index.html        # English home page
│   ├── ru/                   # Russian pages
│   │   └── index.html        # Russian home page
│   └── zh/                   # Chinese pages
│       └── index.html        # Chinese home page
└── test.html                 # Testing page
```

## Key Components

### 1. Multilingual Support

The website is structured to support three languages:
- **English (en)**: Primary language
- **Russian (ru)**: Supporting Eastern European and Central Asian markets
- **Chinese (zh)**: Supporting Asian markets

This is implemented through:
- Language-specific directories in `pages/`
- Language-specific brand profiles in `_brands/`
- Translation data in `_data/translations/`
- Language selector component in `_includes/language-selector.html`

### 2. Collections

The site uses Jekyll collections to organize content:
- **_brands**: Custom collection for brand profiles

### 3. CSS Structure

Instead of using Tailwind CSS, the site implements a vanilla CSS approach:
- `assets/css/basic-colors.css`: Defines color variables and component styles based on the Brandmine color palette

### 4. Layout System

The site uses a simple layout system:
- `_layouts/default.html`: Main layout template that includes header and footer
- Content-specific layouts can be added as needed

### 5. Data Files

Jekyll data files store structured information:
- `_data/sectors.yml`: Defines the 15 business sectors for categorization
- `_data/translations/`: Contains language-specific text for UI elements

## Build and Deployment

The website is built with Jekyll and deployed to GitHub Pages:
1. Local development using `bundle exec jekyll serve`
2. Version control through Git
3. Automatic deployment through GitHub Pages
4. Supporting NPM scripts in `package.json` for development tasks

## Directory Details

### _brands/

This directory contains a custom Jekyll collection for brand profiles, organized by language. Each brand profile is a markdown file with front matter and content describing the brand.

### _data/

Contains structured data used throughout the site:
- `sectors.yml`: Defines the business sectors and their translations
- `translations/`: Contains language-specific text for UI elements

### _includes/

Contains reusable HTML components:
- `header.html`: Site navigation and branding
- `footer.html`: Site footer with additional navigation and copyright
- `language-selector.html`: Component for switching between languages
- `google-analytics.html`: Analytics tracking code

### _layouts/

Contains HTML templates that define the structure of different types of pages:
- `default.html`: Main layout template used by most pages

### pages/

Contains static pages organized by language:
- `en/index.html`: English home page
- `ru/index.html`: Russian home page
- `zh/index.html`: Chinese home page

### assets/

Contains static files like CSS, JavaScript, and images:
- `css/basic-colors.css`: Defines the color system and component styles

## Next Steps

The current structure establishes a foundation for the Brandmine website. Future development will focus on:

1. Populating brand profiles in the `_brands` collection
2. Implementing MapLibre for geographic visualization
3. Connecting to Airtable for dynamic data
4. Enhancing the design and user experience
5. Adding analytics for user behavior tracking

## Technical Notes

1. The site uses vanilla CSS with custom properties (variables) instead of Tailwind CSS for simplicity and reliability.
2. The multilingual structure follows Jekyll best practices for internationalization.
3. Custom collections (`_brands`) are used for organizing brand-specific content.
4. The site is configured for GitHub Pages hosting with a custom domain (via CNAME).
