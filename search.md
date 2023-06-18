---
layout: default
title: Search
description: What're ya buyin?
---

## Got some rare things on sale, stranger! 

<script src="{{ site.baseurl }}/assets/js/jekyll-search.js"></script>

<script>
    SimpleJekyllSearch({
      searchInput: document.getElementById('search-input'),
      resultsContainer: document.getElementById('search-results'),
      json: '{{ site.baseurl }}/search.json',
      searchResultTemplate: '<li><a href="{{ site.baseurl }}/{url}">{title}</a></li>',
      noResultsText: 'No results found',
    });
  </script>

<form id="search-form" role="search">
    <input type="search" id="search-input" placeholder="Search" autocomplete="off">
  </form>


  <div id="search-results"></div>


[back](./)