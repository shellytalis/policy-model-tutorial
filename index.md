---
layout: default
title: Home
nav_order: 1
description: "Policy Models Tutorial."
permalink: /
---

# Focus on ...
{: .fs-9 }

Policy Models Tutorial gives a documentation...
{: .fs-6 .fw-300 }

[Get started now](#getting-started){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [View it on GitHub](https://github.com/EilonBenIshay/PolicyModelsProjectFrontend2022){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## Getting started

### How it looks like...

<img width="335" alt="צילום מסך של האתר" src="https://user-images.githubusercontent.com/48415128/158069121-13250618-4f39-468d-a442-c9198fc3e6c8.png">

### Quick start: Use a Html tag

1. In the "body" tag on your html page, add a html tag that called "policy-models-default" like this:

```yaml
<policy-models-default name="PolicyModels">
    </policy-models-default>
```

<small> There is an attribute "name" that specifies the name of the element. In our case it is PolicyModels.

### Add Style

1. In the html tag "policy-models-default" add:
    
```yaml
 <div id="style"> #nameOfFile# </div>
```
    
2. In the #nameOfFile# you need to write the name of the css file that describes the style that you want the site to have. For example, if the name of the file is "style" that it will be like this:
    
```yaml
<div id="style">style.css</div>
```
    
  [How to write the css file]
    
3. _Optional:_ Initialize search data (creates `search-data.json`)
```bash
$ bundle exec just-the-docs rake search:init
```
3. Run you local Jekyll server
```bash
$ jekyll serve
```
```bash
# .. or if you're using a Gemfile (bundler)
$ bundle exec jekyll serve
```
4. Point your web browser to [http://localhost:4000](http://localhost:4000)

If you're hosting your site on GitHub Pages, [set up GitHub Pages and Jekyll locally](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll) so that you can more easily work in your development environment.



---

## About the project

Just the Docs is &copy; 2017-{{ "now" | date: "%Y" }} by [Patrick Marsceill](http://patrickmarsceill.com).

### License

Just the Docs is distributed by an [MIT license](https://github.com/pmarsceill/just-the-docs/tree/master/LICENSE.txt).

### Contributing

When contributing to this repository, please first discuss the change you wish to make via issue,
email, or any other method with the owners of this repository before making a change. Read more about becoming a contributor in [our GitHub repo](https://github.com/pmarsceill/just-the-docs#contributing).



### Code of Conduct

Just the Docs is committed to fostering a welcoming community.

[View our Code of Conduct](https://github.com/pmarsceill/just-the-docs/tree/master/CODE_OF_CONDUCT.md) on our GitHub repository.

