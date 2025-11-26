# Carson Kohlbrenner - Personal Website

A Jekyll-powered personal academic website.

## Structure

```
ckohl10.github.io/
├── _config.yml          # Jekyll configuration
├── _data/               # YAML data files (easy to update!)
│   ├── papers.yaml      # Publications/research papers
│   ├── projects.yaml    # Academic/personal projects
│   └── news.yaml        # News/Impacts carousel items
├── imgs/               # Image assets (organized by type)
│   ├── papers/          # Images for publications
│   ├── projects/        # Images for projects
│   ├── news/            # Images for news/impacts
│   └── profile/         # Profile photo(s)
├── _includes/           # Reusable HTML components
│   ├── paper.html       # Template for paper entries
│   ├── project.html     # Template for project entries
│   └── impact.html      # Template for impact/news items
├── _layouts/            # Page layouts
│   └── default.html     # Base HTML layout
├── data_new/            # PDF files (CV, papers, etc.)
├── index.html           # Main page template
├── stylesheet.css       # Styling
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## Adding New Content

### Adding a New Paper

Edit `_data/papers.yaml` and add a new entry at the **top** of the file:

```yaml
- id: unique-paper-id    # Used for hover effects (no spaces)
  title: "Your Paper Title"
  authors:
    - name: Your Name
      url: null
      highlight: true    # Set true to bold your name
    - name: Co-Author Name
      url: https://coauthor-website.com
  venue: "Conference or Journal Name"
  year: 2025
  image: imgs/papers/paper-id/cover_image.png
  project_page: https://project-page.com    # Optional
  code: https://github.com/repo            # Optional
  arxiv: https://arxiv.org/abs/xxxx.xxxxx  # Optional
  paper: data_new/paper.pdf                # Optional (local PDF)
  description: "Brief description of the paper."
```

### Adding a New Project

Edit `_data/projects.yaml` and add a new entry at the **top** of the file:

```yaml
- id: unique-project-id
  title: "Your Project Title"
  authors:
    - name: Your Name
      url: null
      highlight: true
    - name: Collaborator
      url: https://collaborator-site.com
  context: "Course Name or Context"
  year: 2024
  image: imgs/projects/project-id/cover_image.png
  paper: data_new/report.pdf    # Optional
  code: https://github.com/repo # Optional
  article: https://medium.com/article  # Optional
  description: "Brief description of the project."
```

### Adding a News/Impact Item

Edit `_data/news.yaml` and add a new entry at the **top** of the file:

```yaml
- id: unique-impact-id
  title: "Impact Title"
  subtitle: "Related Project Name"
  year: 2025
  image: imgs/news/news-id/cover_image.jpg
  alt: "Image alt text for accessibility"
  link: https://related-link.com
  description: "Description shown on hover."
```

## Local Development

### Prerequisites

- Ruby (2.7 or later)
- Bundler (`gem install bundler`)

### Setup

```bash
cd ckohl10.github.io
bundle install
```

### Running Locally

```bash
bundle exec jekyll serve
```

Visit `http://localhost:4000` in your browser.

### Building for Production

```bash
bundle exec jekyll build
```

The static site will be generated in the `_site/` directory.

## Deployment

### GitHub Pages

This site is configured to work with GitHub Pages. Simply push to your `main` branch and GitHub will automatically build and deploy the site.

If using GitHub Pages' built-in Jekyll support, update the `Gemfile`:
1. Comment out `gem "jekyll", "~> 4.3"`
2. Uncomment `gem "github-pages", group: :jekyll_plugins`

### Manual Deployment

Run `bundle exec jekyll build` and upload the contents of `_site/` to your web server.

## Credits

Site template originally built by [Jon Barron](https://github.com/jonbarron).
