## 基于特征融合的无人驾驶感知实时与鲁棒性研究


featured-tags: true  

This website summarizes the topics discussed in our [Paper](https://github.com/b-xie/). References can be navigated by the main topics Sensor fusion / Detection / Segmentation /NAS/ Un/Semi supervision. For Detection and Segmentation meaningful tags are provided to view a subset only (e.g. 2D). Further test vehicle setup are summarized.


index        |      Classification        |	     Segmentation          |  Detection                  |  Vehicles     |Datasets
------------ | -------------
real-time  | [NAS](https://github.com/b-xie/b-xie.github.io/blob/master/_posts/2021-08-30-class_nas.md)<br>Manual<br> Un/Semi supervision<br>Compression<br>Camera<br>LiDAR  | NAS<br>Manual<br> Un/Semi supervision<br>Compression<br>Camera<br>LiDAR <br> Thermal |  NAS<br>Manual<br> Un/Semi supervision<br>Compression<br>Camera<br>LiDAR <br> Thermal<br> Radar<br>3D   |![image](https://user-images.githubusercontent.com/60713917/131202414-9f2a0ac4-f795-4411-ae57-2759f3687556.png)|![image](https://user-images.githubusercontent.com/60713917/131202429-0a746be5-4799-4d37-8227-8a47c4268619.png)
robustness   | Manual<br>Camera<br>LiDAR  | Manual<br>Camera<br>LiDAR <br> Thermal |  Manual<br>Camera<br>LiDAR <br> Thermal<br> Radar<br>3D   | |


You can use the [editor on GitHub](https://github.com/b-xie/b-xie.github.io/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/b-xie/b-xie.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

---
layout: page
description: "自律/坚持/耐心"
---

{% for post in paginator.posts %}
<div class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
        <h2 class="post-title">
            {{ post.title }}
        </h2>
        {% if post.subtitle %}
        <h3 class="post-subtitle">
            {{ post.subtitle }}
        </h3>
        {% endif %}
        <!-- 是否展示文章正文前200个字 -->
        <!--<div class="post-content-preview">
            {{ post.content | strip_html | truncate:200 }}
        </div>-->
    </a>
    <p class="post-meta">
        Posted by
        {% if post.author %}
        {{ post.author }}
        {% else %}
        {{ site.title }}
        {% endif %}
        on {{ post.date | date: "%B %-d, %Y" }}
    </p>
</div>
<hr>
{% endfor %}

<!-- Pager -->
{% if paginator.total_pages > 1 %}
<ul class="pager">
    {% if paginator.previous_page %}
    <li class="previous">
        <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">
            <span class="glyphicon glyphicon-arrow-left" aria-hidden="true">
            </span>
            Newer Posts
        </a>
    </li>
    {% endif %}
    {% if paginator.next_page %}
    <li class="next">
        <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">
            Older Posts
            <span class="glyphicon glyphicon-arrow-right" aria-hidden="true">
            </span>
        </a>
    </li>
    {% endif %}
</ul>
{% endif %}
