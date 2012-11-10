<header>
  <form role="search" method="get" id="searchform" action="http://www.google.com.hk/cse">
    <fieldset role="search">
        <input type="hidden" name="cx" value="{{ site.google_search_id }}"/>
        <input id="sea" class="search" type="text" name="q" results="0" placeholder="Search"/>
    </fieldset>
  </form>
  <div class="hgroup">
      <h1><a href="/">{{ site.title }}</a></h1>
      {% if site.subtitle %}
          <span class="hidden">{{ site.subtitle }}</span>
        {% endif %}
      <a class="feedrss" href="{{ site.subscribe_rss }}">Feed Rss</a>
    </div>
    <div class="menu">
      <ul>
        <li class="page_item"><a href="/" title="首页">首页</a></li>
        <li class="page_item"><a href="/archive.html">Archive</a></li>
        <li class="page_item"><a href="/categories.html">Categories</a></li>
        <li class="page_item"><a href="/tags.html">Tags</a></li>
        <li class="page_item"><a href="/about.html">About</a></li>    
      </ul>
    </div>
</header>