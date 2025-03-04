---
title: Complete Guide to Setting Up RSS Feed on Blogspot | RSS Feed Blogger
tags:
  - ''
private: false
updated_at: ''
id: null
organization_url_name: null
slide: false
ignorePublish: false
---
The URL for Google Blogger RSS feeds is a subdomain of blogspot.com. You might think that the URL is a subdomain of blogger.com. You are wrong! Because Google Blogger is just a CMS (content management system) and requires a domain host to deliver content to users. BlogSpot.com is also owned by Google but is not a CMS, but rather a domain hosting service used by blogger.com.

Therefore, many Blogger websites are accessed from BlogSpot subdomains, so they have a blogSpot.com URL, for example datainchi.blogspot.com. So the difference between blogger and blogspot is clear. To be clearer, Google BlogSpot is used to host content created on Blogger.
- **Blogspot:** domain name (host) used by blogger sites. You can replace the blogspot domain name with the domain you purchased from the hosting service.
- **Blogger:** a CMS that manages the layout of content or articles that will be displayed on the website.

##  A. What is RSS Feed?
RSS feed also known as "Really Simple Syndication feed" is an XML based format for your content. Every time you publish a new post on your blogger, it will be updated in the RSS feed.

The content stored by RSS feed can consist of title, post, Post link, date, and comments. All RSS Feed documents are stored in XML format. Information from various sources presented in RSS format can be collected, processed and presented to the user in a convenient form through special programs called "aggregators".

The basic purpose of a site feed is to allow readers to receive the latest content from your blog. Readers can receive changes to your blog content using the RSS Feed link (URL) that you will create and provide on your blog site. Readers can copy the RSS Feed link and add it to their blog or email.

Not only bloggers provide RSS Feeds, you can also subscribe to RSS Feeds from online RSS Feed providers such as My Yahoo, Feedly, NewsGator, Netvibes, Shrook, FeedWind, RSSOwl, and others.

You can use RSS Feeds in various ways:
1. Display directly from your blogger or
2. Use other platforms such as Amazon Author Central.

In addition, you can also configure [the RSS widget](https://www.inchimediatama.org/2024/10/membuat-widget-postingan-acak-random.html) on your blog to display the latest blog posts or comments on your blog, and can also create a custom HTML sitemap for your blog if your blog RSS Feed is enabled.

Google also has a free RSS Feed called Google FeedBurner. Google FeedBurner is a free feed management service that allows you to create a Feed URL (RSS/Atom), so that people can subscribe or add your site's feed URL on their blog/website/app/browser, etc., to receive the latest content and notifications. Discussion about FeedBurner, we wrote separately, you can read it in the next article.

## B. History of RSS Feeds
[RSS FEED](https://www.inchimediatama.org/2025/01/rss-feed-feedburner-blogger.html) has been around since the late 1990s, but it didn’t really catch on until blogging became more popular in the early 2000s. Since then, many websites have adopted RSS Feeds to distribute their content.

Since the rise of blogging, Google has made it easy to add RSS Feeds to your website so that visitors can easily subscribe to your content updates. With customizable templates and an easy-to-use editor, you can create a beautiful website with RSS feeds in just minutes. What makes RSS Feeds so important?

Before answering the question above, let’s first review how RSS Feeds work. RSS Feeds are a web-based technology that allows publishers to syndicate their content automatically. This technology uses a standard format called XML (Extensible Markup Language) to publish frequently updated information such as blog posts, news articles, podcasts and more.

To use RSS Feeds, you need an aggregator or reader to collect and display the Feed content in one place. Aggregators can be web-based or desktop applications that allow users to subscribe to multiple Feeds from different sources.

When a new article or post is published on a website with an RSS Feed, the aggregator will automatically detect it and display it in its interface. This feature makes it easy for users to stay up to date with their favorite websites without visiting each site individually.

## C. How to Use RSS Feeds from Blogger Sites
All Blogger websites have their RSS Feed enabled by default. You can access it easily by typing the correct URL in your browser.

Blogger supports two Feed formats, RSS Feed and Atom Feed. Out of the two, the most popular and widely used is RSS Feed.

You can use different RSS feeds for different works. For example, you can share all posts, share comments, share posts by labels, or share comments by posts.

All you need is the Feed URL. You can see the example below and access the Feed URL from the website by simply changing the domain name. Below we have provided the URL of the RSS Feed used by bloggers.

**Full site feed:**
**Atom 1.0:** https://datainchi.blogspot.com/feeds/posts/default
**RSS 2.0:** https://datainchi.blogspot.com/feeds/posts/default?alt=rss

**RSS Feed for comments only:**
**Atom 1.0:** https://datainchi.blogspot.com/feeds/comments/default
**RSS 2.0:** https://datainchi.blogspot.com/feeds/comments/default?alt=rss

**RSS Feed with label:**
**Atom 1.0:** https://blogname.blogspot.com/feeds/posts/default/-/[label]
**RSS 2.0:** https://blogname.blogspot.com/feeds/posts/default/-/[label]?alt=rss

After you know the types of RSS Feeds used by Blogger, you may also ask how to use the RSS Feed on Blogger. Although by default Blogger has implemented RSS Feed, but if you do not set it in the Blogger template, the RSS Feed will not work perfectly.

To activate RSS Feed on Blogger, please open your template script. Then you add the following script between <head> and </head>.

```
<link expr:href='data:view.url.canonical + &quot;feeds/posts/default&quot;' expr:title='data:blog.title + &quot; - Atom&quot;' rel='alternate' type='application/atom+xml'/>  
<link href='https://www.blogger.com/feeds/5256982816786471234/posts/default' rel='service.post' title='UNIX LINUX EXPLORE - Atom' type='application/atom+xml'/>  
<link expr:href='data:view.url.canonical + &quot;feeds/posts/default?alt=rss&quot;' expr:title='data:blog.title + &quot; - RSS&quot;' rel='alternate' type='application/rss+xml'/>  
<link expr:href='data:view.url.canonical + &quot;feeds/posts/default?alt=rss&quot;' expr:title='data:blog.title + &quot; - Feed&quot;' rel='alternate' type='application/rss+xml'/>    
<link expr:href='data:view.url.canonical + &quot;feeds/comments/default?alt=rss&quot;' expr:title='data:blog.title + &quot; - Comments Feed&quot;' rel='alternate' type='application/rss+xml'/>    
<link expr:href='data:view.url.canonical + &quot;feeds/comments/default&quot;' expr:title='data:blog.title + &quot; - Comments Atom&quot;' rel='alternate' type='application/rss+xml'/>
<data:blog.feedLinks/>
```

The number 5256982816786471234 is the id number of your blog, you must replace this number according to your blog id.

Because you are using Google's default RSS Feed or Google's standard, so the RSS Feed menu on your blogger dashboard is left as default, you don't need to change it. Unless you are using FeedBurner.

An example of using RSS Feed on Blogger is usually placed in the Footer section as shown in the image below.

![alt text](/home/ns4/Downloads/Example-of-using-RSS-Feed-on-Blogger.png)

## Benefits of RSS Feeds
In this section, you will learn some of the benefits of site feeds.

1. RSS Feeds can increase blog traffic by bringing visitors back to your blog. Most publishers allow the post title and some of the post content to be displayed in the feed. To read the full content of a post, someone must click on its URL to open it on your blog.
2. It can automate the process of sending post content. You don't have to manually send updates to subscribers and websites. The updates are sent and received automatically.
3. It can act as a blog sitemap which means it makes it easier for search engines like Google, Bing, and others to index your content by taking data from the RSS Feed you create.
4. Readers can only get the things they want to read in one place from various sources.
5. Readers are reluctant to subscribe via email, but not to subscribe to RSS Feeds because you are not required to reveal your email address when subscribing to a Feed. This means you are protected from spam, viruses, identity theft, etc.
6. You can display your favorite blog updates/content on your blog.
7. If you have more than one blog, you can display updates/content on other blogs. This means you can send traffic from one blog to another.
8. You can create more than one site feed URL for your blog. Multi-niche blogs create separate category feed URLs, so people can subscribe and receive updates only from the category or categories they want.

Jadi, itulah yang dimaksud dengan pengaturan RSS Feed di Blogger. Dengan pengaturan RSS Feed di Blogger, anda telah membantu konten anda agar cepat di indek oleh Google GSC. Jadi mulai sekarang atur tempalte blog anda agar ditambahkan dengan script RSS Feed yang telah kami bahas di atas.

