VideoObject is a data type in Schema.org that is commonly used to structure information about video clips. This data type allows webmasters and web developers to describe video files in a way that allows search engines and other platforms to better understand and index the content of articles containing video objects.

Using VideoObject can increase the visibility of videos in search engines and speed up the indexing of your article posts by Google. When video information is structured using this type, it helps search engine algorithms extract and display more relevant results. For example, videos can be displayed as thumbnails or carousels in search results, increasing the likelihood that users will click on them.

VideoObject includes various properties that allow you to search for information about the video. For example, you can specify the video title, description, duration, language, authorship, and other important attributes. This makes the information more complete and informative for users and search engines.

In addition, VideoObject can be used in other types of contexts in the Schema.org data structure, allowing you to create more complex and layered descriptions of content. For example, a video can be linked to a specific article, event, or product, further increasing its contextual relevance.

Overall, VideoObject is an essential tool for optimizing video content on the Internet, helping to increase its accessibility and visibility for users and search engines. To structure the Video Carousel data, we need the ItemList property. With ItemList the process of creating a video Carousel becomes easier.

In this article we will explain how to create a Carousel data structure for VideoObject. As a case study we will use Google Blogger to implement the Carousel.

## What is ItemList Schema?
In simple terms, [ItemList Schema](https://www.inchimediatama.org/2024/10/cara-menambahkan-peringkat-bintang.html) is used to mark a list of Items. The list can be of any type, say movies, products, apps, songs, etc., but all list items must have the same Schema type. You can also read the complete definition of ItemList in Schema. Movies. Recipes.

Multiple Items in the ItemList schema are required to structure the data with the Carousel data structure. The first step you need to define is ItemList and ListItem.
- **ItemList:** ItemList is a list that contains all the properties in the list.
- **ListItem:** List of all the elements like URl, type, name, position.
- **item.name:** Name of the item. Like movie name or recipe name.
- **item.url:** Fully qualified URL of the item page.
- **item:** individual property in the list. Like, Movie, Restaurant or recipe.
- **position:** specifies the position of the item in the carousel structure.

While Carousel Structured Data is a display of search results like a horizontal list. Google's search engine usually presents a movie carousel with content images, titles, and release years. It also uses this for books and many others.

Carousels are list-like rich results that people can swipe through on mobile devices. They display multiple cards from the same site (also known as a hosted carousel). To enable carousels for your site, add Carousel structured data in combination with one of the supported content types.

## Where can carousel data be used?
You can use Carousel markup for your website data structure to organize content data such as:
1. Movies
2. Courses
3. Recipes
4. Restaurants
5. Videos (Clips or Youtube)

## How is Carousel Schema implemented?
To implement carousel markup on your website, it is important to decide which pages of your website will carry the markup.
1. Summary Page: This page contains a mini description or summary of each item or itemList where each item in the list has three properties (type, position, and URL).
2. Details Page: This page provides a detailed description of the data using carousel for data structuring. Example: if the summary page is about the best Pineapple cake recipe, then each detail page will have a RECIPE structured data property for that particular recipe.
3. Single List/ All in one page: This is a single page entity that contains all the information related to the carousel. This is a single page link.

## Create Youtube VideoObject Schema Carousel Script in Blogger
As we have explained above, in this example we will practice the Youtube Video Carousel scheme for Google blogger. Although we apply this Carousel Scheme in blogger but you can also use it in other templates such as Joomla, Drupal, Gohugo and others.

Below is an example of a Carousel scheme script for Youtube Videos.
```
<b:includable id='metacarouselvideo' var='posts'>
<b:tag name='script' type='application/ld+json'>
{
&quot;@context&quot;:&quot;http://schema.org&quot;,
&quot;@type&quot;:&quot;ItemList&quot;,
&quot;itemListElement&quot;:
                    [
<b:loop index='i' values='data:posts' var='post'>
{
&quot;@type&quot;:&quot;ListItem&quot;,
&quot;position&quot;:<b:eval expr='data:i + 1'/>,
  
  &quot;item&quot;: {
  &quot;@type&quot;: &quot;VideoObject&quot;,
  &quot;name&quot;: &quot;<data:post.title.jsonEscaped/>&quot;,
  &quot;contentUrl&quot;: &quot;<data:post.url.canonical/>&quot;,  
  &quot;embedUrl&quot; : [&quot;https://youtu.be/0_PiolxXngw&quot;, &quot;https://youtu.be/zcdBK0_mEks&quot;, &quot;https://youtu.be/APHKg0Sv5ls&quot;, &quot;https://youtu.be/ex_HBaVgwiQ&quot;, &quot;https://youtu.be/xX7fupNKc14&quot;, &quot;https://youtu.be/8yib19VUbJA&quot;, &quot;https://youtu.be/Bdhh5grAtBk&quot;, &quot;https://youtu.be/KUJxf2utxlQ&quot;],
  <b:if cond='data:post.thumbnailUrl'>  
  &quot;thumbnailUrl&quot; : [&quot;https://img.youtube.com/vi/0_PiolxXngw/mqdefault.jpg&quot;, &quot;https://img.youtube.com/vi/zcdBK0_mEks/mqdefault.jpg&quot;, &quot;https://img.youtube.com/vi/APHKg0Sv5ls/mqdefault.jpg&quot;, &quot;https://img.youtube.com/vi/ex_HBaVgwiQ/mqdefault.jpg&quot;, &quot;https://img.youtube.com/vi/xX7fupNKc14/mqdefault.jpg&quot;, &quot;https://img.youtube.com/vi/8yib19VUbJA/mqdefault.jpg&quot;, &quot;https://img.youtube.com/vi/Bdhh5grAtBk/mqdefault.jpg&quot;, &quot;https://img.youtube.com/vi/KUJxf2utxlQ/mqdefault.jpg&quot;],  
  
&quot;thumbnail&quot;: &quot;<b:eval expr='data:post.thumbnailUrl'/>&quot;,
<b:else/>
&quot;thumbnail&quot;: &quot;https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgPDiGLN0WIVlBM4MWvmlAodRyGl94YerRvht_KaclgWxr6iBV387QY9KXiCheLF335MU5YJVht3rWP0NCQI7U9gPbIt7iRFKwhiP_eHjFjrvdhtsPEh4z3w0-gyLl0w96NCOPX_XjGDjgRikZh2xxfQU0ShdfZfw8cpvaq4SMO0vMToslIoAIOOqF53QI/s320/Mohon%20maf%20artikel%20ini%20tak%20ada%20gambar.jpg&quot;,   
&quot;thumbnailUrl&quot;: &quot;https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgPDiGLN0WIVlBM4MWvmlAodRyGl94YerRvht_KaclgWxr6iBV387QY9KXiCheLF335MU5YJVht3rWP0NCQI7U9gPbIt7iRFKwhiP_eHjFjrvdhtsPEh4z3w0-gyLl0w96NCOPX_XjGDjgRikZh2xxfQU0ShdfZfw8cpvaq4SMO0vMToslIoAIOOqF53QI/s320/Mohon%20maf%20artikel%20ini%20tak%20ada%20gambar.jpg&quot;,
</b:if>
&quot;uploadDate&quot;: &quot;<data:post.date.iso8601.jsonEscaped/>&quot;,
&quot;description&quot;: &quot;<data:post.snippet.jsonEscaped/>&quot;
}
}
<b:if cond='data:i != data:posts.length - 1'>,
</b:if></b:loop>
  ]

  }
</b:tag>
</b:includable>
```

In the script example above, the "embedUrl" code is the URL address of your video content on YouTube. The more videos you upload to YouTube, the longer the "embedUrl" code.

You can place the script above anywhere above the </body> code, but the script above is not active or you cannot use the script. In order to use the script, you must activate the script.

To activate the script, look for the code "<b:includable id='post' var='post'>" and type the following script below the code above.

```
<b:if cond='data:posts.length &gt; 0'>
<b:include cond='data:view.isMultipleItems' data='posts' name='metacarouselvideo'/>  
</b:if>
```

For troubleshooting issues, Google Search Console is your best friend and will help you with all your issues. Using carousels to structure your data not only makes it unique but also makes users visit your website again and again. If you are confused about which schema or structured data type to use to structure your website or webpage, you can always refer to our previous post that discusses [Schema.org](https://schema.org/) data structure.


