# PIANO website

Repository of the static site generation code for the project PIANO, via [Jekyll](https://jekyllrb.com/).

For simple content changes, it should be enough to modify and commit changes, as a GitHub action should re-generate the site upon push to the default branch. For more complex changes it is better to use a local Jekyll installation.

## Content management

To simply add or modify content: clone the repository, make changes, commit, and push to the main branch.

### News posts

In the website section `News`, each entry is a [Jekyll post](https://jekyllrb.com/docs/posts/). Markdown is the preferred format to create posts and these are shown in reverse chronological order.

To add an entry, in the `_posts` directory create a file with the following name format:

```
YEAR-MONTH-DAY-my-title.md
```

At the top of the file, the following YAML frontmatter must be present:

```yaml
---
layout: post
title:  "My Title"
author: Firstname Lastname
image: /assets/imgs/posts/my_post_image.jpg
---
```

The field `image` is optional. If present, this image will be used for the SEO metadata of the post. To insert this image in your post as a figure, use the following liquid code:

```liquid
{% include post_fig.html src=page.image alt="My post image alt description" caption = "My post image figure caption" %}
```

Both `alt` and `caption` parameters are customizable and optional. The post's main image must have a maximum width of 1080 pixels, but preferably less. Other images used in the post can have a higher resolution if their dimension properties are set appropiately.

The first paragraph of the post will be used as the respective excerpt in the `News` section an SEO metadata.

### Publications

Edit `_bibliography/references.bib`. The latest publication should be at the top of the file, as the order in this file is the order in which the contents will appear on the website. The bibliography style is APA.

If a bibliography entry has the field `url` set, it will be used to generate an external `Link`. If an entry has the field `arxiv`, which should be set to the arXiv identifier of the publication (i.e., `2312.10269`), it will be used to generate an external link `arXiv` to the preprint. Both fields `url` and `arxiv` can be used at the same time, but these should not link to the same preprint in arXiv.

### Partners and People

Edit `_data/partners.yml`. The order in this file is the order in which the contents will appear on the website, for both partners and people.

#### Person picture

A corresponging picture for each person should be in the respective partner subdirectory in `assets/imgs/people/`, with the following requisites:

- filename must be `firstname_lastname.jpg`
- image must be square, with a resolution of 400×400 pixels
- image background must be light-colored

If a picture file is not found, a placeholder will be used instead.

## Local Jekyll installation

Prerequisites:

- Ruby language (v3.x preferred)
- Jekyll 4.3.x

See the official [Jekyll installation documentation](https://jekyllrb.com/docs/installation/#requirements) for more details.


## Contributors

[Amaury Trujillo](https://www.iit.cnr.it/en/amaury.trujillo/) - creator and maintainer