---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: home
---

## 历史版本

{% for release in site.github.releases %}

### {{release.tag_name | capitalize}}

{%- for asset in release.assets %}

#### {{ asset.updated_at | date: site.minima.date_format }} [{{ asset.name }}]({{ asset.browser_download_url }})

{%- endfor %}
{% endfor %}
