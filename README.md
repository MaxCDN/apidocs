# MaxCDN API docs

## Page structure

### /docs

Docs page uses `default.html` template. The file structure is as follows:

**Head**

```
/_includes
|-- header.html (page meta)
|-- includes.html (CSS/font refs)
```

**Content**

Page title, page content, main containers and rows are written here.

```
/_includes
|-- navbar.html (Logo and navigation)
|-- sidebar.html (sidebar for non-reseller clients)
|-- docs.md (complete content of the page)
|-- footer.html (JS files)
```
**docs.md (page content)**

Markdown file which contains the complete content. Content which is written in Markdown is labeled as [Index].

```
[Index]
[Overview]
[Support]
[Changelog]
/_includes
|-- authentication.md
|-- account.md
|-- zones.md
|-- reports.md
|-- rawlogs.md
|-- originshield.md
|-- ssl.md
```

### /reseller

Reseller page uses `page.html` template. The file structure is as follows:

**Head**

```
/_includes
|-- header.html (page meta)
|-- includes.html (CSS/font refs)
```

**Content**

Page title, main containers and rows are written here.

```
/_includes
|-- navbar.html (Logo and navigation)
|-- sidebar-reseller.html (sidebar for reseller clients)
|-- reseller.md (complete content of the page)
|-- footer.html (JS files)
```

**reseller.md (page content)**

Markdown file which contains the complete content. Content which is written in Markdown is labeled as [Index].

```
[Index]
[Overview]
[Support]
[Changelog]
/_includes
|-- authentication.md
|-- account.md
|-- zones.md
|-- reports.md
|-- rawlogs.md
|-- originshield.md
|-- ssl.md
|-- clients.md
```

## Layouts

Layouts can be found in the `_layouts` folder. Default ones are:

* default.html
* page.html
* post.html

`default.html` and `page.html` are used for this website and they contain HTML code which includes main containers and includes.

## Preparation

1. Install git (if you don't have it installed already)
2. Navigate to the local folder where you would like to store the project, clone the repository and edit it locally:

`$ git clone https://github.com/MaxCDN/apidocs.git`

3. Ensure that all upcoming commits are made in `gh-pages` branch:

`$ git checkout gh-pages`

## Workflow

The branch `gh-pages` is the main Git branch that is recognized by GitHub. All code inside `gh-pages` branch will be processed by Liquid (templating engine) on GitHub's end every time a new push is performed. The end result will be deployed on the live site.

When performing any kind of changes (adding/removing text, editing CSS and similar files), it's preferable to make all changes inside the `master` branch, test the changes locally and then merge the changes with the `gh-pages` branch when finished with editing. Performing a `git push` will push the changes to the main GitHub repository and changes will be reflected on the live site after purging the pull zone cache.

### Switching to master branch

`$ git checkout master`

### Merging the changes into gh-pages

`$ git checkout gh-pages`

`$ git merge master`

## Adding content

### Pages

1. Create a new .html file (it can be in any directory, but doesn't have to)
2. Create a new .md file for Markdown content (empty)
3. Add the following code to the .html file

```	
---
layout: layout_name
title: page_title
permalink: /relative/path
---
{% capture variable_name %} {% include markdown.md %} {% endcapture %}
{{ variable_name | markdownify }}
```

* `layout_name` within `layout: layout_name` is the name of the file found in `_layouts` folder and it should be put without extension (filename.ext => filename)
* `title: page_title` is meta for page title you are creating
* `permalink: /relative/path` is a location to HTML file created in step #1
* `filename` within `{% capture variable_name %}` is a custom variable that is filled with the value of `{% include markdown.md %}` where `filename.md` is the Markdown file (if you have one - not mandatory to have it) and then calling `markdownify` with `{{ variable_name | markdownify }}` you are building the content defined in Markdown file (markdown.md)

4. Push on Git

`$ git add .`

`$ git commit -m 'comment'`

`$ git push`

### Page content

Page content should be added to the corresponding .md files (docs.md or reseller.md). Markdown can be used both in main .md files and in modules.

#### Markdown syntax
##### Standard tags

`#` - h1

`##` - h2

`###` - h3

`content(#link)` - Link

`Paragraph` - No markup

#### Tables
	
```
Column 1 Content | Column 2 Content | Column 3 Content | 
--- | --- | ---
```
	
uses highlighted style for the previous row

##### Includes

`{% include modulename.ext %}` (file should be in _includes folder)

#### Sidebar

Sidebar content is included from `_includes/sidebar.html` (sidebar-reseller.html for Reseller page). Sidebar content is inputted in the following divisions:

```
<div class="span3">
	<div id="docs-navbar" data-spy="affix" data-offset-top="201">
		<div class="row">
			<div class="span3">
				<ul class="nav nav-pills nav-stacked">
``` 

Example li:

```
<li><a href="#overview">Overview</a></li>
```

Example ul:

```
<ul class="nav-bold nav-down hide">
	<li class="nav-sub"><a href="#auth-overview" class="gotohash">Overview</a></li>
</ul>
```

Links in sidebar include `a href` which refers to an anchor on the page (i.e. `<a id="auth-overview">`). IDs are automatically added through jQuery for `h` elements (`h1`, `h2`, etc.).

#### API Method and Endpoint section

Example:

```
<div class="heading">
	<div class="url GET"><span class="http_method">GET</span>
	<span class="path">https://rws.maxcdn.com/{companyalias}/account.json</span></div>
</div>
```

#### Tabbed content

Each new section should increment the class number for `ul` and `li`.

Example:

If tabbed menu with `myTab` exists, new tabbed menu should have `myTab2`. All elements within `myTab2` unordered list should have the same index (`ruby2`, `python2`, etc.).

#### Tabs

```
<ul class="nav nav-tabs" id="myTab1">
	<li class="active"><a href="#ruby1" data-toggle='tab'>Ruby</a></li>
	<li><a href="#python1" data-toggle='tab'>Python</a></li>
	<li><a href="#perl1" data-toggle='tab'>Perl</a></li>
	<li><a href="#php1" data-toggle='tab'>PHP</a></li>
	<li><a href="#node1" data-toggle='tab'>Node</a></li>
	<li><a href="#csharp1" data-toggle='tab'>.NET/C#</a></li>
	<li><a href="#response1" data-toggle='tab'>Response</a></li>
</ul>
```

**Important: Ensure that first *li* element has active class as well, so it's the focused tab on the current page section!**

Example:

```
<li class="active"><a href="#ruby1" data-toggle='tab'>Ruby</a></li>
```

#### Tabs content

```
<div class="tab-content">
	<div class="tab-pane active" id="ruby1">
		<pre>
			//Your code goes here
		</pre>
	</div>
	...
</div>
```

**Important: Ensure that first `tab-pane` div has active class as well so it matches with the focused tab above!**

Example:

```
<div class="tab-pane active" id="ruby1">
```

**Important: Code within `<pre>` tags will print indentation and white spaces so avoid adding spaces or [tabs] before the text itself because, it will be indented twice (or more).**

## Restoring to previous revision

In case the content should be reverted to one of the previous revisions, follow these steps:

1. Go to [https://github.com/MaxCDN/apidocs/tree/gh-pages](https://github.com/MaxCDN/apidocs/tree/gh-pages) in browser
2. Click on “X commits” above the file listing, where X is the number of commits that were made to the repository.
3. Locate the desired revision and copy it’s hash from the right. In the example the hash is `e57638e`
4. Make sure that the changes are made to gh-pages:

`$ git checkout gh-pages`

5. Initiate reset using the hash of the selected revision:

`$ git reset e57638e`

## Preview

Website will be built and available on:

[http://maxcdn.github.io/apidocs/docs/](http://maxcdn.github.io/apidocs/docs/)

[http://maxcdn.github.io/apidocs/reseller/](http://maxcdn.github.io/apidocs/reseller/)

The changes will not be visible on [docs.maxcdn.com](docs.maxcdn.com) and [reseller.docs.maxcdn.com](reseller.docs.maxcdn.com) until the CDN Pull Zone is purged.
