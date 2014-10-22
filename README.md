# Mon Jekyll carbure au Pixyll

[pixyll.com](http://www.pixyll.com) A Jekyll theme by [John Otander](http://johnotander.com)
([@4lpine](https://twitter.com/4lpine)).

It's mobile _first_, fluidly responsive, and delightfully lightweight.

It's pretty minimal, but leverages large type and drastic contrast to make a statement, on all devices.


## TUTOS sur Jekyll

[Smashing Magazine](http://www.smashingmagazine.com/2014/08/01/build-blog-jekyll-github-pages/).

### Using Github Pages

You can host your Jekyll site for free with Github Pages. [Click here](https://pages.github.com/) for more information.

#### A configuration tweak if you're using a gh-pages sub-folder

In addition to your github-username.github.io repo that maps to the root url, you can serve up sites by using a gh-pages branch for other repos so they're available at github-username.github.io/repo-name.

This will require you to modify the `_config.yml` like so:

```yml
# Site settings
title: Repo Name
email: your_email@example.com
author: John Otander
description: "Repo description"
baseurl: "/repo-name"
url: "http://github-username.github.io"

# Build settings
markdown: kramdown
permalink: pretty
paginate: 3
```

This will ensure that the the correct relative path is constructed for your assets and posts. Also, in order to run the project locally, you will need to specify the blank string for the baseurl: `$ jekyll serve --baseurl ''`.

##### If you don't want the header to link back to the root url

You will also need to tweak the header include `/{{ site.baseurl }}`:

```html
<header class="site-header px2 px-responsive">
  <div class="mt2 wrap">
    <div class="measure">
      <a href="{{ site.url }}/{{ site.baseurl }}">{{ site.title }}</a>
      <nav class="site-nav right">
        {% include navigation.html %}
      </nav>
    </div>
  </div>
</header>
```

A relevant Jekyll Github Issue: <https://github.com/jekyll/jekyll/issues/332>

### Page Animation

If you would like to add a [fade-in-down effect](http://daneden.github.io/animate.css/), you can add `animated: true` to your `_config.yml`.

### Put in a Pixyll Plug

If you want to give credit to the Pixyll theme with a link to <http://pixyll.com> or my personal website <http://johnotander.com> somewhere, that'd be awesome. No worries if you don't.

### Enjoy

I hope you enjoy using Pixyll. If you encounter any issues, please feel free to let me know by creating an [issue](https://github.com/johnotander/pixyll/issues). I'd love to help.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Thanks to the following:

* [BASSCSS](http://basscss.com)
* [Jekyll](http://jekyllrb.com)
* [Refills](http://refills.bourbon.io/)
* [Solarized](http://ethanschoonover.com/solarized)
* [Animate.css](http://daneden.github.io/animate.css/)
