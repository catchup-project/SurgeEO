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
1. [Stupid-quick Start Guide](/Surgeapps/Surge-E-O#stupid-quick-start-guide)
2. [Tag Reference](/Surgeapps/Surge-E-O/wiki/Tag-Reference)
3. [Usage Examples](/Surgeapps/Surge-E-O/wiki/Usage-Examples)
4. [Config Options: Global Defaults](/Surgeapps/Surge-E-O/wiki/Configuration)
5. [Config Options: Additional](/Surgeapps/Surge-E-O/wiki/Configuration)

###Addendum
---
1. How to use global headers
2. How we guess the entry_id





Stupid-Quick Start Guide
---

**Global Header Include:**

```
<head>
	<title>{title}</title>
	<meta name="keywords" content="{keywords}" />
	<meta name="description" content="{description}" />
</head>
```

**Some template:**

```
{embed="site/_header" 
	title="{exp:seo:title url_title='{segment_3}'}" 
	keywords="{exp:seo:title url_title='{segment_3}'}" 
	description="{exp:seo:title url_title='{segment_3}'}"
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
