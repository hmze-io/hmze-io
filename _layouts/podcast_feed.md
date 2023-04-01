<?xml version="1.0" encoding="UTF-8"?>
<rss xmlns:itunes="http://www.itunes.com/dtds/podcast-1.0.dtd" xmlns:media="http://search.yahoo.com/mrss/" xmlns:atom="http://www.w3.org/2005/Atom" xmlns:content="http://purl.org/rss/1.0/modules/content/" xmlns:googleplay="http://www.google.com/schemas/play-podcasts/1.0" version="2.0">
  <channel>
    <atom:link href="https://pubsubhubbub.appspot.com/" rel="hub"/>
    <atom:link href="{{ site.feed_url | absolute_url }}" rel="self"/>
    <atom:link href="{{ site.feed_url | absolute_url }}" rel="first"/>
    <atom:link href="{{ site.feed_url | absolute_url }}" rel="last"/>
    <title>{{ site.title }}</title>
    <language>{{ site.feed_lang }}</language>
    <pubDate>{{ site.feed_since }}</pubDate>
    <lastBuildDate>{{ site.posts[0].date | date: "%a, %d %b %Y %H:%M %z" }}</lastBuildDate>
    <description>{{ site.description }}</description>
    <link>{{ site.website_url | absolute_url }}</link>
    <generator>{{ site.website_url | absolute_url }}</generator>
    <itunes:type>episodic</itunes:type>
    <image>
      <url>{{ site.logo | absolute_url }}</url>
      <title>{{ site.title }}</title>
      <link>{{ site.website_url | absolute_url }}</link>
    </image>
    <itunes:image href="{{ site.logo | absolute_url }}"/>
    <itunes:subtitle/>
    <itunes:author>{{ site.feed_owner}}</itunes:author>
    <itunes:explicit>no</itunes:explicit>
    <itunes:keywords></itunes:keywords>
    <itunes:category text="Technology"/>
    <itunes:category text="News">
      <itunes:category text="Tech News"/>
    </itunes:category>
    <itunes:summary>{{ site.description }}</itunes:summary>
    <itunes:owner>
      <itunes:name>{{ site.feed_owner }}</itunes:name>
      <itunes:email>{{ site.feed_contact }}</itunes:email>
    </itunes:owner>
    {{ content }}
  </channel>
</rss>