# StewartKnapman.com

Personal website built with [Siteleaf v2](http://www.siteleaf.com)

Issues thus far:
- Can't get a page object by slug/handle/id: `{% assign my_page = site.pages.my_page %}` or `{% assign my_page = site.pages['my_page'] %}`
- ~~Can't get the whole page object: `{% assign home = site.pages | where: 'title', 'Home' %}` just returns the pages content~~ Correct usage is `{% assign home = site.pages | where: 'title', 'Home' | first %}`
- Can't make dynamic defaults in front matter i.e. `handle: "{{ page.title | slugify }}"` (explore https://github.com/gjtorikian/jekyll-conrefifier ?)