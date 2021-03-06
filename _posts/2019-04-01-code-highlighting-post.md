---
title: New ImageNET SOTA
layout: post
excerpt: Next level results on classic DL tasks
categories:
  - code
modified: '2014-09-14'
comments: true
---

# 2019-04-01-code-highlighting-post

Syntax highlighting is a feature that displays source code, in different colors and fonts according to the category of terms. This feature facilitates writing in a structured language such as a programming language or a markup language as both structures and syntax errors are visually distinct. Highlighting does not affect the meaning of the text itself; it is intended only for human readers.

### Example of embedded tweet

Jeremys point in below is brilliant is brilliant but not

.[@LiberalAlliance](https://twitter.com/LiberalAlliance?ref_src=twsrc%5Etfw) og [@alternativet\_](https://twitter.com/alternativet_?ref_src=twsrc%5Etfw)'s rejse fra 0 - 7,5 pct.[\#dkpol](https://twitter.com/hashtag/dkpol?src=hash&ref_src=twsrc%5Etfw) [\#polling](https://twitter.com/hashtag/polling?src=hash&ref_src=twsrc%5Etfw) [\#rstats](https://twitter.com/hashtag/rstats?src=hash&ref_src=twsrc%5Etfw) [pic.twitter.com/Bg3HHjk8SF](https://t.co/Bg3HHjk8SF)— Mikkel Krogsholm \(@mikkelkrogsholm\) [June 19, 2016](https://twitter.com/mikkelkrogsholm/status/744645313655373824?ref_src=twsrc%5Etfw)

### Pygments Code Blocks

To modify styling and highlight colors edit `/_sass/_pygments.scss`.

### Standard Code Block

```text
{% raw %}
<nav class="pagination" role="navigation">
    {% if page.previous %}
        <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
    {% endif %}
    {% if page.next %}
        <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
    {% endif %}
</nav><!-- /.pagination -->
{% endraw %}
```

### Fenced Code Blocks

To modify styling and highlight colors edit `/_sass/_coderay.scss`. Line numbers and a few other things can be modified in `_config.yml`. Consult [Jekyll's documentation](http://jekyllrb.com/docs/configuration/) for more information.

```css
#container {
    float: left;
    margin: 0 -240px 0 0;
    width: 100%;;
}
```

```markup
{% raw %}<nav class="pagination" role="navigation">
    {% if page.previous %}
        <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
    {% endif %}
    {% if page.next %}
        <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
    {% endif %}
</nav><!-- /.pagination -->{% endraw %}
```

```ruby
module Jekyll
  class TagIndex < Page
    def initialize(site, base, dir, tag)
      @site = site
      @base = base
      @dir = dir
      @name = 'index.html'
      self.process(@name)
      self.read_yaml(File.join(base, '_layouts'), 'tag_index.html')
      self.data['tag'] = tag
      tag_title_prefix = site.config['tag_title_prefix'] || 'Tagged: '
      tag_title_suffix = site.config['tag_title_suffix'] || '&#8211;'
      self.data['title'] = "#{tag_title_prefix}#{tag}"
      self.data['description'] = "An archive of posts tagged #{tag}."
    end
  end
end
```

