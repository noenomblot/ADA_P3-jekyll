---
layout: page
title: "Reddit Rewired: Event-Driven Interactions"
subtitle: How global events impact Reddit communities
cover-img: /assets/img/reddit_header.png
---


# When the World Breaks In: How Reddit Reacts to Major Events

Have you ever opened Reddit expecting something light — maybe a few cute pet photos — only to find yourself pulled into the breaking news of an earthquake on the other side of the world?

Or started your scroll casually, only to realize that *something big* is happening, simply because every corner of your feed feels different?

That’s Reddit.

---

## A Network That Feels Chaotic — But Isn’t

At first glance, Reddit can feel overwhelming. Thousands of communities. Millions of users. Endless posts, links, arguments, jokes, and memes.

Yet beneath this apparent chaos lies a surprisingly structured system.

Reddit is not just a collection of isolated forums — it is a **dense network of hyperlinks**, where communities constantly reference one another, intentionally or not. And when a major world event occurs, this network doesn’t stay still.

It **reacts**.

---

## Collective Attention in Motion

Elections, unexpected product launches, breaking news, global crises — when moments like these happen, millions of people turn to the internet to make sense of them. They comment, debate, explain, speculate, and joke.

Reddit becomes a living map of collective attention.

But this raises an essential question:

> **How does attention move across the platform?**

- Do communities that usually ignore each other suddenly connect?
- Do political spaces spill into entertainment or gaming communities?
- Once the event passes, do these connections disappear — or do they leave behind a lasting trace?

---

What makes Reddit especially powerful for this kind of analysis is its **organized structure**. Each subreddit acts as a semi-independent community, yet hyperlinks create bridges between them.

This allows us to observe:
- **Micro-scale behavior**: how individual communities react and reference others.
- **Macro-scale patterns**: how entire clusters of communities shift during major events.

In other words, Reddit lets us watch collective behavior **form, spread, and decay** in real time.

---

## Let’s Dive In

By following the flow of hyperlinks across Reddit before, during, and after major world events, we can begin to understand how digital communities respond to shocks — much like societies do in the real world.

So let’s zoom out, map the network, and explore how Reddit reacts when the world suddenly demands everyone’s attention.



## Turning Reddit Data Into a Living Network

What you may not know is that Reddit quietly accumulates vast amounts of data — and putting that data to good use is what we do best. Using the **SNAP Hyperlink Network dataset**, we track how subreddits reference one another through shared hyperlinks, and we pair these connections with the sentiment that travels alongside them. The result is not just a graph of links, but a **network of interactions**, where attention, emotion, and information move together.

---

## Clearing the Noise: When Bots Get in the Way

Unfortunately, the modern internet is not populated by humans alone. It is crowded with automated accounts designed to farm engagement, collect clicks, and inflate visibility. If Reddit is to be treated as a mirror of the real world, this noise has to go.

Before modeling collective behavior, the network must first be cleaned.

---

## Finding Humans in a Sea of Automation

To uncover genuine, human-driven dynamics, abnormal posting behavior is first separated from the rest. Each subreddit is described through a rich set of signals that capture **how content is written**, **how often it is posted**, and **how sentiment evolves over time**. Together, these signals form a high-dimensional behavioral fingerprint.

Because many of these characteristics overlap or move together, the data is compressed into a more compact representation that preserves what matters most. By keeping only the components that explain the vast majority of observed variation, the complexity is reduced without erasing the patterns that distinguish organic activity from automation.

<figure class="figure text-center">
  <img src="assets/img/explained_variance.png"
       alt="Explained variance as a function of the number of principal components"
       width="600">
  <figcaption class="figure-caption">
    Cumulative explained variance as a function of the number of principal
    components. The dashed line indicates the 90% variance threshold.
  </figcaption>
</figure>
<br>

Within this simplified space, irregular behavior begins to stand out. Highly automated subreddits tend to follow narrow, repetitive patterns, making them easier to isolate than the messier, more diverse behavior of human communities. Subreddits that repeatedly exhibit these signatures are flagged as bot-heavy and filtered out of the network.

The accompanying visualization highlights the fifteen subreddits with the highest estimated levels of automated activity — the noisiest corners of the platform.

<figure class="figure text-center">
  <img src="assets/img/Top15subreddits.png"
       alt="Top 15 subreddits by bot-like post rate"
       width="700">
  <figcaption class="figure-caption">
    <strong>Figure 4.</strong> Top fifteen subreddits ranked by the proportion of
    posts flagged as bot-like by the Isolation Forest model. High values indicate
    subreddits where automated activity is likely to dominate content production,
    motivating their exclusion from subsequent network analyses.
  </figcaption>
</figure>
<br>

---

## From Chaos to Communities

With bots removed, the Reddit Hyperlink Network is more authentic — but it is still vast, tangled, and nearly impossible to navigate at the level of individual subreddits.

So the perspective shifts.

Instead of focusing on thousands of small communities, hyperlink interactions are grouped into **broader categories of human interest**: politics, sports, gaming, world news, and beyond. At this scale, the network starts to look familiar. Some communities emerge as bridges during moments of intense attention, channeling information across otherwise distant topics. Others remain inward-looking, largely unaffected by external events.



<div class="flourish-embed flourish-hierarchy" data-src="visualisation/26914732">
  <script src="https://public.flourish.studio/resources/embed.js">
  </script>
  <noscript>
    <img src="https://public.flourish.studio/visualisation/26914732/thumbnail" width="100%" alt="hierarchy visualization" />
  </noscript>
</div>

Connections form quickly when the world demands attention, intensify as conversations converge, and then either fade away or settle into more permanent pathways — depending on the nature of the event that sparked them.
---

## A Structure That Suddenly Makes Sense

Seen from a distance, the structure of Reddit snaps into focus. Thousands of subreddits merge into a smaller number of recognizable communities, each reflecting a facet of human curiosity.

This is why, on Reddit, it feels perfectly normal to learn about a new restaurant opening while searching for a gaming tutorial — or to stumble upon a season finale spoiler while trying to figure out how to farm Bitcoin in your basement.

What looks like randomness is, in fact, a network quietly shaped by shared attention.

<div class="flourish-embed flourish-network" data-src="visualisation/26916638">
  <script src="https://public.flourish.studio/resources/embed.js">
  </script>
  <noscript>
    <img src="https://public.flourish.studio/visualisation/26916638/thumbnail" width="100%" alt="network visualization" />
  </noscript>
</div>


<!-- The file is under _includes/intercluster.md -->
{% include intercluster.md %}



<!-- The file is under _includes/intra_cluster_analysis.md -->
{% include intra_cluster_analysis.md %}



---

## In conclusion

The Reddit Hyperlink Network, once examined through rigorous analysis, reveals itself to be far more complex than it first appears. What often feels like a space for absent-minded scrolling — a way to momentarily escape the real world — turns out to be a remarkably faithful mirror of it.

Within this network, communities form, evolve, and interact in ways that closely resemble offline social systems. They argue, align, fragment, and occasionally converge around shared moments. World events act as catalysts, pulling attention inward and reshaping how communities relate to one another. Some connections are strengthened through shared focus and collective engagement, while others are strained or weakened as disagreement and emotional intensity rise.

Major events leave the deepest structural footprints. Elections, crises, and globally shared moments reorganize attention at scale, forging links that can persist long after the headlines fade. Yet smaller, more localized events matter too. Even when their impact does not propagate across an entire cluster, they still leave measurable traces within individual communities, briefly redirecting attention and altering internal dynamics.

Across all levels of analysis — between clusters, within clusters, and between specific communities — one pattern remains consistent: Reddit does not react uniformly. Attention spreads unevenly, influence flows asymmetrically, and engagement depends on context, relevance, and perceived importance. In this way, the platform behaves less like a chaotic feed and more like a living social network, shaped by the same selective pressures that govern real-world interaction.

So the next time you follow a hyperlink to another subreddit, pause for a moment before scrolling past. That click may pull you into the center of an unfolding conversation — one that strengthens old ties, challenges existing narratives, or reshapes the structure of a community altogether. In doing so, you become part of the same collective dynamics that quietly turn Reddit into a map of the world it reflects.


## References

<ul>
  <li>
    SNAP – Stanford Network Analysis Project.  
    <i>Reddit Hyperlinks Network (soc-RedditHyperlinks)</i>.  
    Available at:
    <a href="https://snap.stanford.edu/data/soc-RedditHyperlinks.html" target="_blank">
      https://snap.stanford.edu/data/soc-RedditHyperlinks.html
    </a>.
  </li>
</ul>

