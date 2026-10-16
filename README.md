# This is the source for my site

It is a [Jekyll](https://jekyllrb.com) based static site. The site is built
locally and the generated files are published to the `gh-pages` branch, which
GitHub Pages serves as-is at https://agpelliza.github.io.

- `master` holds the source (this branch).
- `gh-pages` holds only the generated site. Don't edit it by hand; `bin/deploy`
  overwrites it.

## Layout

| Path | What it is |
|---|---|
| `_config.yml` | Site settings (Markdown engine, URL, excluded files) |
| `_layouts/` | Page templates: `default.html` wraps every page, `post.html` wraps posts |
| `_posts/` | Blog posts, one Markdown file each |
| `_drafts/` | Unpublished posts (ignored by git) |
| `guides/`, `experiences/` | Index pages listing posts of that category |
| `references/`, `random/` | Standalone pages |
| `css/`, `img/` | Static assets, copied as-is |
| `atom.xml` | The feed |
| `bin/deploy` | Builds the site and publishes it to `gh-pages` |

## Setup

You need Ruby 3.3 or newer and Bundler. On macOS with Homebrew:

```bash
brew install ruby@3.3
export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"
export LANG=en_US.UTF-8
```

Put the two `export` lines in your shell profile so they persist. The system
Ruby that ships with macOS is too old.

Then install the gems:

```bash
bundle install
```

## Preview locally

```bash
bundle exec jekyll serve --livereload
```

Open http://localhost:4000. Pages rebuild when you save a file; changes to
`_config.yml` need a restart. Add `--drafts` to include posts from `_drafts/`.

## Write a post

1. Create `_posts/YYYY-MM-DD-short-title.md` (or start it in `_drafts/`
   without the date prefix).
2. Start it with front matter and the usual heading:

   ```markdown
   ---
   layout: post
   title: My New Post
   category: guides
   ---

   {{ page.title }}
   ----------------

   <p class="meta">16 Oct 2026 - Buenos Aires, Argentina</p>

   The post body...
   ```

   `category` is `guides` or `experiences`; it decides which index page lists
   the post and its URL (`/guides/2026/10/16/my-new-post.html`).
3. For code samples use a fenced block with a language, or
   `{% highlight bash %} ... {% endhighlight %}`.
4. Preview it, then commit it to `master`.

## Deploy

```bash
bin/deploy
```

The script refuses to run with uncommitted changes, so commit first. It then:

1. builds the site with `JEKYLL_ENV=production` into `_site/`,
2. copies `_site/` into the `gh-pages` branch (adding `.nojekyll` so GitHub
   serves the files without rebuilding them),
3. commits as `Deploy <source commit>` and pushes `gh-pages`.

The site updates a minute or so after the push. Pushing `master` alone does not
change the live site, so push it too to keep the source backed up:

```bash
git push origin master
```

GitHub Pages must be set to serve from the `gh-pages` branch, root folder
(Settings → Pages → Build and deployment → Deploy from a branch). This is a
one-time setting.

## Update dependencies

```bash
bundle outdated
bundle update
bundle exec jekyll build
```

Check the build output and preview the site, then commit `Gemfile.lock` and
deploy. Before a major Jekyll upgrade (e.g. 4.x → 5.x), read the upgrade notes
at https://jekyllrb.com/docs/upgrading/.

## Troubleshooting

- **`Invalid US-ASCII character`**: the shell isn't using UTF-8. Set
  `LANG=en_US.UTF-8`.
- **`ruby ... is incompatible with the current version` or gems failing to
  install**: you're on the macOS system Ruby. Check `ruby -v` and fix your
  `PATH` as shown in Setup.
- **The live site didn't change after deploying**: check that GitHub Pages is
  serving the `gh-pages` branch, and look for the latest run on the repo's
  Actions tab.
