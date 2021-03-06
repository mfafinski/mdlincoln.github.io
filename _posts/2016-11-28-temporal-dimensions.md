---
layout: post
title: '"The Temporal Dimensions of the London Art Auction" in _British Art Studies_'
date: 2016-11-28T08:37:17-08:00
comments: true
tags:
- art history
- articles
- digital humanities
- r
---

I'm incredibly pleased to say that a paper co-authored with my awesome UMD colleague Abram Fox is finally out today, open access, in [_British Art Studies_](http://britishartstudies.ac.uk/issues/issue-index/issue-4/london-art-auction-1870-1835).
The life cycle of this article, by the way --- 2.5 years in the making --- witnessed two new jobs, an entire dissertation, and (way more impressive) the birth of an honest-to-goodness child.

The abstract:

>The rush of activity among London's auction houses in the first few weeks of summer has long been a familiar occurrence that persists even today.
However, this intense seasonal concentration of sales was not always so.
This paper draws on quantitative methods to explore the gradual emergence of a tightly scheduled auction season in London at the turn of the nineteenth century, focusing on the sale of paintings.
Through the use of historical auction catalogue data, the paper traces the ways in which this shift varied across different segments of the auction market, as well as between individual auction houses.
As our study shows, the temporal clustering of painting auctions had specific business advantages, but it also played a key role in enhancing the social import of these auctions, demarcating an annual, weeks-long "event" looked to with anticipation and excitement by auctioneers and buyers alike.

### The Back Story

The germ of this project came from a [post on this blog back in March of 2014](/2014/03/17/doing-the-season-historic-art-sale-calendars.html) when I had first started toying with art historical data in general, and specifically, looking at the historical sales catalog data from the [Getty Provenance Index](http://www.getty.edu/research/tools/provenance/search.html).
Just looking at a small subset of painting auctions by Christie's, I was not surprised to see that the aggregate sales landed during the late spring and early summer - the traditional period of the London "Season".
What _was_ surprising was to see that this concentration changed somewhat over time - enough to get me talking to Abram in order to learn some more about this history.

But these early histograms were only hints at a possible finding.
They were not anything substantial in their own right.
To understand the details of how this seasonal concentration may have occurred - who was driving it, and for which kinds of sales - we needed to [operationalize](https://litlab.stanford.edu/LiteraryLabPamphlet6.pdf) the way that we gauged seasonality.
By transforming this judgment from a hazy, visual impression of a series of histograms (i.e. what we had in the original blog post) into a summary metric (the year-to-year change in the coefficient of variation of top sales days), it became possible to calculate that summary metric across a matrix of different variables.
This helped us quickly distill which sections of the market, and which players, were driving the effects we saw in the original aggregate.

{% include figure.html caption="Visualizing the change in the coefficient of variation the of top auction days between 1780 and 1835. [View in the context of the paper.](https://doi.org/10.17658/issn.2058-5462/issue-04/afox-mlincoln/figure7)" src="/assets/images-display/bas_cv.png" %}

This is a dead-simple operationalization compared to complex textual or network or image analysis.
But even simple operationalizations like this are crucial for our discipline.
Already I am looking for ways to improve this study in follow-up work.
For example, it needs to better account for the uncertainty introduced by missing information.
[This is a problem we are actively working on now with a wider array of Getty data as part of the Getty Provenance Index Remodeling project.](http://blogs.getty.edu/iris/metadata-specialists-share-their-challenges-defeats-and-triumphs/#matt)
Furthermore, if we see this complexity of seasonal structures in London, what was going on in Paris, or Berlin at this same time?

If you would like to see the mechanics of how we transformed these data, you can consult our [supplemental material](https://github.com/mdlincoln/londonauctions), which includes raw and transformed datasets, as well as a walkthrough of the cleaning and plotting code.
One note: while the supplemental material includes everything you need to reproduce our results, the figures on the finished _British Art Studies_ article are actually rendered in JavaScript, thanks to the careful work of the editors (Tom Scutt in particular) at _BAS_.
[You can read more about their interest in the affordances of digital publishing in their issue editorial.](http://britishartstudies.ac.uk/issues/issue-index/issue-4/editorial-4)
In the (likely) event that those renderings break in the next few years, you will always be able to find the static variants archived on GitHub and Zenodo.
