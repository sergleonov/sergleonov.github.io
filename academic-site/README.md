# Sergei Leonov — academic website

A small Jekyll site that GitHub Pages builds automatically. It ships with its own minimal theme ("academic") and can switch to any GitHub Pages theme or community Jekyll theme with two lines in `_config.yml`.

## Publish it

1. Create a GitHub repo named `sergleonov.github.io`.
2. Copy these files into it and push.
3. In the repo, go to **Settings → Pages**, set **Source** to "Deploy from a branch", pick `main` and `/ (root)`.
4. The site appears at `https://sergleonov.github.io` within a minute or two.

## Edit content

| What | Where |
|---|---|
| Name, affiliation, links | `_config.yml` |
| Bio | `index.md` |
| News | `_data/news.yml` |
| Papers | `_data/publications.yml` |
| Projects (add repo links here) | `_data/projects.yml` |
| Research, teaching, awards | `cv.md` |
| Photo | `assets/img/` (then update `photo:` in `_config.yml`) |
| CV PDF | `assets/files/cv.pdf` |

Content is independent of the theme, so none of these change when you switch.

## Switch themes

In `_config.yml`, uncomment one `theme:` or `remote_theme:` line and set the default layout to match:

| Theme | Config line | `layout:` |
|---|---|---|
| Built-in academic (default) | none | `academic` |
| GitHub themes: minimal, cayman, slate, architect, dinky, hacker, leap-day, merlot, midnight, modernist, tactile, time-machine | `theme: jekyll-theme-minimal` (etc.) | `default` |
| Minima | `theme: minima` | `page` |
| Minimal Mistakes | `remote_theme: mmistakes/minimal-mistakes` | `single` |
| Any other theme on GitHub | `remote_theme: owner/repo` | see its README |

Browse the GitHub themes at https://pages.github.com/themes/ and community themes at http://jekyllthemes.org.

How it works:

- The built-in theme lives in `_layouts/academic.html` and `assets/css/academic.css`. Their names don't collide with any theme's files, so they never override a theme you pick.
- `assets/css/content.css` styles the news, publication and project lists. `_includes/head-custom.html` (GitHub themes) and `_includes/custom-head.html` (Minima) load it inside other themes too, so publications keep their formatting.
- Navigation differs by theme. The academic theme reads `nav` in `_config.yml`, Minima reads `header_pages`, and Minimal Mistakes uses `_data/navigation.yml` (see its docs). GitHub's themes show the site title and description but no menu.
- The sidebar profile (photo, email, Scholar) is part of the academic theme. Other themes show their own header instead; most read `title`, `description` and `author` from `_config.yml`.

Community themes like al-folio and academicpages are full templates you fork rather than themes you load, so they don't plug in this way.

## Preview locally (optional)

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.
