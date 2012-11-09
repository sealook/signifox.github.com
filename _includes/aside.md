<aside>
      <ul id="side" class="clear">
        <li class="widget">
          <div class="license">
            <p><img class="aligncenter" class="center" alt="License" src="/media/image/nc-sa-2.5.png" /></p>
            <p>本站所有作品采用
              <a href="http://creativecommons.org/licenses/by-nc-sa/2.5/cn/">知识共享署名-非商业性使用-相同方式共享 2.5 中国大陆许可协议</a>
              进行许可。
            </p>
          </div>
        </li>
        <li class="widget">
          <h3 class="widgettitle">分类目录</h3>
          <ul class="categories">
              {% for cat in site.categories %}
                <li><a href="/categories.html#{{ cat[0] }}-ref" title="{{ cat[0] }}" rel="{{ cat[1].size }}">{{ cat[0] }} <sup>({{ cat[1].size }})</sup></a></li>
              {% endfor %}
          </ul>
        </li>
        <li class="widget">
          <h3 class="widgettitle">标签云</h3>
           <p>
              <div id='tag_cloud'>
                {% for tag in site.tags %}
                <a href="/blog/tags.html#{{ tag[0] }}-ref" title="{{ tag[0] }}" rel="{{ tag[1].size }}">{{ tag[0] }} 
                <sup>({{ tag[1].size }})</sup>
                </a>
                {% endfor %}
            </div>
          </p>
          <script language="javascript">
             $.fn.tagcloud.defaults = {
              size: {start: 1, end: 2, unit: 'em'}
            };
          $(function () {
            $('#tag_cloud a').tagcloud();
          });
          </script>
        </li>
        <li class="widget">
          <h3 class="widgettitle">近期文章</h3>
          <ul class="posts">
            {% for post in site.posts limit: 5 %}
              <li><a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
            {% endfor %}
          </ul>
        </li>
        <li class="widget">
          <h3 class="widgettitle">近期评论</h3>
          <ul class="comments">
            <script type="text/javascript" src="http://shawhu.disqus.com/recent_comments_widget.js?num_items=5&hide_avatars=0&avatar_size=32&excerpt_length=50">
            </script>
          </ul>
        </li>
        <li class="widget">
          <h3 class="widgettitle">友情链接</h3>
          <ul class='blogroll'>
            <li><a href="http://saipingwen.org">猴子</a>  超级大牛</li>
            <li><a href="http://www.baidu.com">百度</a></li>
            <li><a href="http://www.cplusplus.com/reference">CPP Reference<a></li>
          </ul>
        </li>
      </ul>
</aside>