SurgeEO SEO Add-On for ExpressionEngine 2
---

###What is it?
---
SurgeEO is an add-on that lets you add SEO meta data to your site pages, and control those in the admin area. You can edit/control:

1. Title tag
2. Description Meta Tag
3. Keywords Meta Tag
4. Canonical Tag
5. Robots (Privacy from search bots)

###What problems does SurgeEO solve?
---
We created an SEO plugin because we implement best SEO practices in all of our client sites. There are few high-quality add-ons, and we saw some of them doing too much, or lacking in important areas. Here were our goals:

1. Easily administrate SEO data in the admin area (duh)
2. Use best practices - Don't make using a global header hard
3. Administrate SEO data to aggregate pages - Those with no specific entry assigned **(This one is exciting!)**

###Documentation
---
1. [Stupid-quick Startup Guide](#stupid-quick-startup-guide) - Even a caveman can do it...
2. [Tag Reference](../../wiki/Tag-Reference) - All available tags
3. [SEO data for Entries](../../wiki/SEO-for-Entries) - Adding SEO data to your entries
4. [SEO data for Pages](../../wiki/SEO-for-Pages) - Adding SEO data to pages with no entry!
3. [Usage Examples](../../wiki/Usage-Examples) - Usage examples to get you underway quickly
4. [Config Options: Global Defaults](../../wiki/Configuration) - Basic Options
5. [Config Options: Additional](../../wiki/Configuration) - Additional Options
6. [FAQ](../../wiki/FAQ)

###Addendum
---
1. How to use global headers
2. How we guess the entry_id





Stupid-Quick Startup Guide
---

**Global Header Include:**

```html
<head>
	<title>{embed:title}</title>
	<meta name="keywords" content="{embed:keywords}" />
	<meta name="description" content="{embed:description}" />
</head>
```

**Some template:**

```html
{embed="site/_header" 
	title="{exp:surgeeo:title url_title='{segment_3}'}" 
	keywords="{exp:surgeeo:keywords url_title='{segment_3}'}" 
	description="{exp:surgeeo:description url_title='{segment_3}'}"
}
<body>
	<div class="container">
		<div class="row">
			{exp:channel:entries channel="some_channel"}
			<article>
				<h2>{title}</h2>
				{content}
			</article>
			{/exp:channel:entrie}
		</div>
	</div>
</body>
```
