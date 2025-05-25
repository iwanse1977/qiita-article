> [!WARNING]
> **The `master` branch is under active development towards a semver-major release with non-backwards-compatible changes.**
> 
> While you may use this theme in the current state either via the `jekyll-remote-theme` plugin or via a Gemfile, it is
> recommended to point to a particular git ref that does not break your site's existing render and gradually update to a
> newer git ref via a pull request after consulting this repository's commit-log and README.
>
> **Pointing directly to the `HEAD` commit of the `master` branch is risky and may contain changes that break your site.** 
>
> Example of pointing to a particular git ref via `jekyll-remote-theme` plugin:
> ```yaml
> # _config.yml
>
> remote_theme: "jekyll/minima@1e8a445"
> ```
> Example of pointing to a particular git ref via `Gemfile` (with `theme: minima` in `_config.yml`)
> ```ruby
> # Gemfile
>
> gem "minima", github: "jekyll/minima", ref: "1e8a445"
> ```

<br/><br/>

<div align="center">
  <p><em><strong>Disclaimer:</strong> The information here may vary depending on the version you're using.<br/>
  Please refer to the <code>README.md</code> bundled within the theme-gem for information specific to your version or by pointing
  your browser to the Git tag corresponding to your version. e.g. https://github.com/jekyll/minima/blob/v2.5.0/README.md.<br/>
  Running <code>bundle show minima</code> will provide you with the local path to your current theme version.</em></p>
  <img src="/readme_banner.svg"/>
  <p>It's Jekyll's default (and first) theme. It's what you get when you run <code>jekyll new</code>.</p>
  <p><a href="https://jekyll.github.io/minima/">Theme preview</a></p>
  <p><img src="/screenshot.png"/></p>
</div>

## Installation

Add this line to your Jekyll site's Gemfile:

```ruby
gem "minima"
```

And then execute:

    $ bundle


## Contents At-A-Glance

Minima has been scaffolded by the `jekyll new-theme` command and therefore has all the necessary files and directories to have a new Jekyll site up and running with zero-configuration.

### Layouts

Refers to files within the `_layouts` directory, that define the markup for your theme.

  - `base.html` &mdash; The base layout that lays the foundation for subsequent layouts. The derived layouts inject their
    contents into this file at the line that says ` {{ content }} ` and are linked to this file via
    [FrontMatter](https://jekyllrb.com/docs/frontmatter/) declaration `layout: base`.
  - `home.html` &mdash; The layout for your landing-page / home-page / index-page. [[More Info.](#home-layout)]
  - `page.html` &mdash; The layout for your documents that contain FrontMatter, but are not posts.
  - `post.html` &mdash; The layout for your posts.

#### Base Layout

From Minima v3 onwards, the base layout is named **`base.html`** instead of `default.html` to avoid confusing new users into
assuming that name holds special status.

Users migrating from older versions with customized `_layouts/default.html` are advised to rename their copy to
`_layouts/base.html`. Migrating users with additional customized layouts may either update front matter references to former
`default.html` layout or create a new `default.html` layout referencing the current `base.html`, whichever route being the
easiest:

```
---


### Change default date format

You can change the default date format by specifying `site.minima.date_format`
in `_config.yml`.

```
# Minima date format
# refer to http://shopify.github.io/liquid/filters/date/ if you want to customize this
minima:
  date_format: "%b %-d, %Y"
```


### Extending the `<head />`

You can *add* custom metadata to the `<head />` of your layouts by creating a file `_includes/custom-head.html` in your source directory. For example, to add favicons:

1. Head over to [https://realfavicongenerator.net/](https://realfavicongenerator.net/) to add your own favicons.
2. [Customize](#customization) default `_includes/custom-head.html` in your source directory and insert the given code snippet.


### Enabling comments (via Disqus)

Optionally, if you have a Disqus account, you can render a comments section below each post with the following configuration:

```yaml
url: "https://my_domain.com"
disqus:
  shortname: my_disqus_shortname
```

You can find out more about Disqus' shortnames [here](https://help.disqus.com/installation/whats-a-shortname).

Comments are enabled by default and will only appear in production, i.e., `JEKYLL_ENV=production`

If you don't want to display comments for a particular post you can disable them by adding `comments: false` to that
post's YAML Front Matter.

### Author Metadata

From `Minima-3.0` onwards, `site.author` is expected to be a mapping of attributes instead of a simple scalar value:

```yaml
author:
  name: John Smith
  email: "john.smith@foobar.com"
```

To migrate existing metadata, update your config file and any reference to the object in your layouts and includes as summarized below:

Minima 2.x    | Minima 3.0
------------- | -------------------
`site.author` | `site.author.name`
`site.email`  | `site.author.email`


### Social networks

You can add links to the accounts you have on other sites, with respective icon as an SVG graphic, via the config file.
From `Minima-3.0` onwards, the social media data is sourced from config key `minima.social_links`. It is a list of key-value pairs, each entry
corresponding to a link rendered in the footer. For example, to render links to Jekyll GitHub repository and Twitter account (now X), one
should have:

```yaml
minima:
  social_links:
    - title: Jekyll repository at GitHub
      icon: github
      url: "https://github.com/jekyll/jekyll"
    - title: Jekyll at X (formerly Twitter)
      icon: x-twitter
      url: "https://x.com/jekyllrb"
```

where `title` corresponds to the link-title displayed when a visitor hovers mouse-pointer over url / icon and
`icon` refers to the Font Awesome icon id. e.g. `github` corresponds to `fa-github`.

Social platform icons are rendered using the latest version of Font Awesome Free webfonts sourced via remote CDN.
The full list of available social icons can be found at https://fontawesome.com/search?ic=brands

> [!NOTE]
> The link to your site's main syndication feed is always rendered as the last item of the social-links list.<br />
> You may opt to not have this link rendered at all by setting config **`minima.hide_site_feed_link`** to `true`:
> ```yaml
> minima:
>   hide_site_feed_link: true  # `false` or `null` by default
> ```

### Enabling Google Analytics

To enable Google Analytics, add the following lines to your Jekyll site:

```yaml
google_analytics: G-NNNNNNNNNN  // The former `UA-NNNNNNNN-N` format is no longer supported by Google
```

Google Analytics will only appear in production, i.e., `JEKYLL_ENV=production`.

### Enabling Excerpts on the Home Page

To display post-excerpts on the Home Page, simply set `show_excerpts` under top-level key `minima` to `true` in your
`_config.yml`:

```yaml
minima:
  show_excerpts: true
```


## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/jekyll/minima. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `script/bootstrap`.

To test your theme, run `script/server` (or `bundle exec jekyll serve`) and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme and the contents. As you make modifications, your site will regenerate and you should see the changes in the browser after a refresh.

## License

The theme is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
