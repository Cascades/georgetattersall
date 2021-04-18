---
title: A Japanese Journey (With some webdev)
subtitle: https://ukiyo-emap.com/
date: 2021-04-17T23:45:09.436Z
draft: false
featured: false
external_link: https://georgetattersall.me/project/a-japanese-journey-with-some-webdev
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---
This project is a little different from the other projects on here so far. While I have always aspired to enter the video games industry, specifically in a graphics or engine role, I also have a love of Japanese traditional artwork, ukiyo-e (oo-ki-yo-eh).

A few years ago I was in a C++ job, learning lots about the language and its surrounding technologies full time, and I found myself wanting to develop myself in other technologies in my spare time. At the same time I was also frustrated at the lack of visual maps of Japanese woodblock print locations plotted on a map plotted on maps that were available on the internet. This may sound peculiar, but these prints are often done in series focussed on either a specific location (Mt. Fuji or modern day Tokyo), or along a journey between cities.

A good example of this is Hokusai's "Fifty-three Stations of the Tōkaidō". In the series, the painter of "The Great Wave off Kanagawa" (pictured below) travelled along a Japan's "Tōkaidō" route, which at the time was the most important route in Japan, connecting Tokyo to Kyoto, it's two biggest cities. On foot the journey could take a week, so stations providing food, accommodation, and rest to travellers. These stations were the main focus of Hokusai's illustrations and could be found published nationally as cheaply and affordably as the modern day newspaper.

<!--StartFragment-->

{{< figure src="Tsunami_by_hokusai_19th_century.jpg" caption="The Great Wave off Kanagawa - Not from the Fifty-three Stations of the Tōkaidō, but instead The Thirty-six Views of Mount Fuji." >}}

<!--EndFragment-->

To begin building the site I envisioned I first required reasonably accurate geographical information on the prints contained in these series. At the time I was able to find very precise coordinates for the prints from a website which I embarrassingly cannot find any longer. Nonetheless, at the time the data was convincing enough for me to not feel I would be misleading people.

I then went about scraping the data from the HTML of the site using a custom parsing script. Extracting print data and placing it in a MongoDB instance as I went along.

Now that I had all the data, I started working on a minimal front end. I opted to use a friendly looking JS library for the map backend, and manually played around with the styling until I got something I liked. To fill the website with my data I actually wrote a static site generator from scratch too. This was just because I thought it would be quicker and easier for my *very static* purposes. I'd say it took a week two to three weeks to do the previous three paragraphs, and then I finally purchased a small server to run it off of, purchased a nice URL, and linked it all up!

Some of the results of the site are below, showing a the aforementioned Tōkaidō, as well as the variety of locations in and around Tokyo. [The site itself can be found here.](https://ukiyo-emap.com/)

<!--StartFragment-->

{{< figure src="map1.png" caption="Tōkaidō" >}}

<!--EndFragment-->

<!--StartFragment-->

{{< figure src="map2.png" caption="Edo, modern day Tokyo" >}}

<!--EndFragment-->

During the course of this project I had to tackle a few challenges I'd never solved in practise before. These include:

* Heavy web-scraping
* MongoDB management
* More javascript than I'm used to
* System design considerations (server load, etc.)
* Apache
* Wiring together all the components

I was very satisfied with how this project went, and evidently, so was the public! In the first week of launching, [John Resig](https://twitter.com/jeresig), creator of jQuery, chief architect at KhanAcademy, and "Japanese Woodblock Print nerd" had [tweeted about my site](https://twitter.com/jeresig/status/1087778797422764032). I was over the moon, and it went viral on a very small scale, also being published in [Spoon & Tamago](https://www.spoon-tamago.com/2019/01/23/ukiyoe-interactive-map/), and tweeted about by a variety of other, including [Open Culture](https://twitter.com/openculture/status/1091034938328068096)!

The number of people viewing the site was quite astounding at first, but it has now calmed down to a steady stream, mainly from the US and Japan.

As long as my website has been able to excite at least some people about Japanese woodblock printing, then it's a job well done!