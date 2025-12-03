# Johns Hopkins Algorithms and Complexity Group Website

A modern Jekyll-based website for the JHU Algorithms and Complexity research group, designed for GitHub Pages.

## Local Development

### Prerequisites
- Ruby 2.7+ with Bundler
- Jekyll

### Setup

1. Install dependencies:
   ```bash
   bundle install
   ```

2. Run the development server:
   ```bash
   bundle exec jekyll serve
   ```

3. Open [http://localhost:4000](http://localhost:4000) in your browser.

## Deployment to GitHub Pages

This site should automatically build when you push changes. to the `main` branch of the repository.

### Custom Domain (Optional)

To use a custom domain:
1. Add a `CNAME` file with your domain name
2. Configure DNS settings with your domain provider
3. Update the `url` and `baseurl` in `_config.yml`

## Structure

```
├── _config.yml                 # Jekyll configuration and site metadata
├── Gemfile                     # Ruby dependencies (jekyll, plugins)
├── _data/
│   └── people.yml              # Data-driven people lists (faculty, affiliated, students, alumni)
├── _layouts/
│   └── default.html            # Main layout template (header, nav, footer)
├── _includes/
│   └── person-card.html        # Reusable person card include used by people.md
├── assets/
│   ├── css/
│   │   └── style.css           # Main stylesheet with JHU color variables and responsive design
│   └── images/
│       ├── jhu-shield.svg      # JHU shield used in header
│       ├── shield-white.svg    # White shield used in footer
│       ├── favicon.svg         # Favicon
│       └── people/             # Person photos (e.g., Michael-Dinitz.png)
├── index.md                    # Home page
├── people.md                   # People page (renders entries from `_data/people.yml`)
├── seminar.md                  # Seminar page (manually edited list of talks)
├── favicon.ico                 # Legacy favicon (also included for compatibility)
├── .gitignore                  # Local excludes (e.g., _site/)
└── README.md                   # This file
```

## Updating Content

### Adding or Updating People

People are now driven from `_data/people.yml`. To add or update a person, edit that file and add an entry under the correct section (faculty, affiliated, students, alumni). Each entry supports `name`, `url`, and an optional `role`:

```yaml
faculty:
  - name: John Doe
    url: https://example.com
    role: Professor
```

The site automatically renders `person-card` elements for each person. You can add an entry with just a `name` if there is no link or role.

### Adding a Seminar Talk

Edit `seminar.md` and add a new talk card:

```html
<div class="info-card">
  <h3>Talk Title</h3>
  <p><strong>Speaker:</strong> Speaker Name (Affiliation)</p>
  <p><strong>Date:</strong> Wednesday, Month Day, Year at 12:00 PM</p>
  <p><strong>Location:</strong> Malone 228</p>
  <p><strong>Abstract:</strong> Talk abstract goes here.</p>
</div>
```

### Customizing Colors

The site uses JHU's official colors. Edit the CSS variables in `assets/css/style.css`:

```css
:root {
  --color-primary: #002D72;      /* JHU Blue */
  --color-accent: #CF4520;       /* JHU Spirit Orange */
  /* ... other variables ... */
}
```

## License

This website template is provided for the Johns Hopkins Algorithms and Complexity group.
