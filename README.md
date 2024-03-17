# Zhang Lab @ Cedars-Sinai Webpage Documentation

## 1. Installation & Setup
Our lab webpage is supported by [Jekyll](https://jekyllrb.com/) with a template from [al-folio](https://github.com/alshedivat/al-folio).

You can go to Jekyll's official site to install it first. Depending on your Operating System, this may be different. See the Installation Guide for Jekyll [here](https://jekyllrb.com/docs/installation/).

You will also need Imagemagick for image conversion to enable across-device compatibility. On MacOS, install by `brew install imagemagick`.

Once you have working Jekyll, use the following command-lines:
```
git clone git@github.com:zhanglab-aim/zhanglab-aim.github.io.git
cd zhanglab-aim.github.io
bundle install # this will install all required dependencies
bundle exec jekyll serve .
```

Then go to `localhost:4000` in your browser. Viola!

## 2. Understanding the layout

`_pages`: contains the Markdown source files for pages from navigation bars.

`_news`: contains the Markdown source files for news. Note that if `inline=false`, then the Markdown filename will used as the header line in the News section.

`_members`: contains the Markdown file for each lab member. Profile images are stored in `assets`.

`_software`: each Markdown file is a software bulletin under `software` page.

`_data`: currently only contains the `coauthor.yml` file. Used to highlight co-authors in bibliography.

`assets`: contains resource files, such as image for lab members, or PDF for papers. Files in this folder can be accessed by perma links.

`_layouts`: contains html files that serve as templates for Markdown sources. Typically you don't need to change this, unless you are implementing a new feature.

`_includes`: contains html files that are helpers for `_layouts`. Smaller, reusable html components are stored here.

## 3. Make changes and deploy
Use git to track the changes. Once you are done, you can commit and push as usual to the `main` branch.

However, the changes will not reflect on the GitHub pages (i.e. public view), because GitHub pages is set to track the content in the branch `gh-pages`. To deploy the changes, simply use
```
./bin/deploy
```
.. and follow instructions from command-line outputs. The script will automatically compile the static html files and push to the designated branch for serving.

### 3.1 Update news

Initialize a new Markdown file for news. If `inline=true`, you don't need to worry about the filename and just include a **one-sentence** summary in the Markdown file.

However, if you'd like to add a multi-line news by `inline=false`, make sure to name your Markdown file with an informative, short, one-line filename. Words can be split by dashed "-", and dashes will be split and each word after dash will be capitalized. Otherwise, use space and the words will be displayed as is.


### 3.2 Update publications
First, add an BibTex entry in `_bibliography/papers.bib`. We can go to Google scholar, select a paper, and click Export, and select "BibTex" in the drop-down menu.

You may want to add other information to this BibTex entry, such as HTML link, codes, and journal abbreviations. You can do so by adding these lines like below:
```
@article{zhang2021automated,
  title={An automated framework for efficiently designing deep convolutional neural networks in genomics},
  author={Zhang, Zijun and Park, Christopher Y and Theesfeld, Chandra L and Troyanskaya, Olga G},
  journal={Nature Machine Intelligence},
  volume={3},
  number={5},
  pages={392--400},
  year={2021},
  publisher={Nature Publishing Group},
  # SEE ADDED ENTRIES BELOW
  abbr={Nat. Mach. Intell.},
  html={https://www.nature.com/articles/s42256-021-00316-z},
  code={https://github.com/zj-zhang/AMBER},
  selected={true}
}
```

Then, if this paper is the first paper in a year, you will need to further add it in `_pages/publications.md` in the place below:
```
---
layout: page
permalink: /publications/
title: publications
# ADD YEAR 2022 SO PAPERS FROM 2022 WILL BE DISPLAYED
years: [2022, 2021, 2020, 2019, 2018, 2017, 2013]
nav: true
nav_rank: 4
---
```


#### Troubleshooting
- If the co-authors are not listed properly (say, underscored and hyperlinked), you should go to `_data/coauthors.yml` and update this yaml file.
- If the publications are not listed properly in Team page, you should go to `_members/person.md` and update the `publication:` entry in markdown file.

### 3.3 Update your information

New members can insert their profiles by adding a new Markdown file in `_members`. 
Filename convention should be `firstname_initial.lastname.md`.
Uploade profile pictures to `assets/img/members/`.

Note: profile pictures need to be cropped/reshaped to 800x800 pixels for best display. Use imagemagick convert to rescale the pictures (`convert in.png -resize 800x800 out.png`), and use powerpoint to crop an image into a square.



