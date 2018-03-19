---
title: Content Editor
category: Editing
order: 2
requirements:
  build: Any
  plan: Free
  hosting: Any
---

The *Content Editor* is an elegant rich text editor for Markdown files.
Clients and team members use this to edit formatted Markdown without having to know the syntax or use a plain text editor.

The *Page Selector* shows a list of pages, posts, drafts and collection items to navigate to.
Use the **Toggle Pages** button in the top right corner to access it.

![Content Editor](/images/editing/content-editor.png){: srcset="/images/editing/content-editor.png 800w, /images/editing/content-editor@2x.png 1600w"}
{: .has-screenshot}


### Hiding the Content Area

When files only use the front matter, it is better to display a full screen front matter editor. Toggle the content section in the *Content Editor* using the `_hide_content` variable. Configure it with one of the following methods.

The collection definition in `_config.yml`:

{% highlight yaml %}
collections:
  projects:
    output: false
    _hide_content: true
{% endhighlight %}

Directly in the front matter:

{% highlight markdown %}
---
title: Hello World
_hide_content: true
---
{% endhighlight %}

Jekyll defaults in `_config.yml`:

{% highlight yaml %}
defaults:
  - type: 'projects'
    values:
      _hide_content: true
{% endhighlight %}

![Content Editor with no content section](/images/editing/content-editor-hidden-content.png){: srcset="/images/editing/content-editor-hidden-content.png 800w, /images/editing/content-editor-hidden-content@2x.png 1600w"}
{: .has-screenshot}
