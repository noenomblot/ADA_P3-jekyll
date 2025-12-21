---
layout: page
title: "Reddit Rewired: Event-Driven Interactions"
subtitle: How global events impact Reddit communities
cover-img: /assets/img/reddit_header.png
---

# 1. When the World Breaks In: How Reddit Reacts to Major Events {#part1}

Have you ever opened Reddit expecting something light — maybe a few cute pet photos — only to find yourself pulled into the breaking news of an earthquake on the other side of the world?

Or started your scroll casually, only to realize that *something big* is happening, simply because every corner of your feed feels different?

That’s Reddit.

---

### A Network That Feels Chaotic — But Isn’t

At first glance, Reddit can feel overwhelming. Thousands of communities. Millions of users. Endless posts, links, arguments, jokes, and memes.

Yet beneath this apparent chaos lies a surprisingly structured system.

Reddit is not just a collection of isolated forums — it is a **dense network of hyperlinks**, where communities constantly reference one another, intentionally or not. And when a major world event occurs, this network doesn’t stay still.

It **reacts**.

---

### Collective Attention in Motion

Elections, unexpected product launches, breaking news, global crises — when moments like these happen, millions of people turn to the internet to make sense of them. They comment, debate, explain, speculate, and joke.

Reddit becomes a living map of collective attention.

This raises an essential question:

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

### Let’s Dive In

By following the flow of hyperlinks across Reddit before, during, and after major world events, we can begin to understand how digital communities respond to shocks — much like societies do in the real world.

So let’s zoom out, map the network, and explore how Reddit reacts when the world suddenly demands everyone’s attention.

---

## 2. Turning Reddit Data Into a Living Network {#part2}

Reddit quietly accumulates vast amounts of interaction data — but in its raw form, it’s closer to noise than insight. Using the **SNAP Reddit Hyperlink Network dataset**, we track how subreddits reference one another through shared hyperlinks and pair these connections with the sentiment that travels alongside them. The result is not just a static graph of links, but a **network of interactions**, where attention, emotion, and information move together.

<details class="event-block">
  <summary>
    <span class="event-pill">Data pipeline</span>
    <span>From raw posts to an interaction network</span>
  </summary>
  <div>
    <p>In practice, our pipeline follows a few key steps:</p>
    <ul>
      <li><strong>Source</strong>: Start from the SNAP <em>soc-RedditHyperlinks</em> dataset, which records hyperlinks between subreddits over time.</li>
      <li><strong>Build edges</strong>: Treat each hyperlink as a directed edge from a source subreddit to a target subreddit.</li>
      <li><strong>Attach metadata</strong>: Enrich these edges with additional information such as timestamps and sentiment scores.</li>
      <li><strong>Aggregate over time</strong>: Group interactions into time windows so we can observe how the network evolves before, during and after real-world events.</li>
      <li><strong>Filter &amp; cluster</strong>: Remove bot-dominated subreddits and group the remaining ones into meaningful communities (politics, gaming, world news, etc.), which will become the stage on which events act.</li>
    </ul>
    <p>This gives us a living, time-resolved network that we can probe at different scales.</p>
  </div>
</details>

---

### Clearing the Noise: When Bots Get in the Way

The modern internet is not populated by humans alone. It is crowded with automated accounts designed to farm engagement, collect clicks, and inflate visibility. If Reddit is to be treated as a mirror of the real world, this noise has to go.

Before modeling collective behavior, the network must first be **cleaned**.

---

#### Finding Humans in a Sea of Automation

To uncover genuine, human-driven dynamics, abnormal posting behavior is first separated from the rest. Each subreddit is described through a rich set of signals that capture:

- **How content is written**,  
- **How often it is posted**,  
- **How sentiment evolves over time**.

Together, these signals form a high-dimensional behavioral fingerprint for each subreddit.

Because many of these characteristics overlap or move together, the data is compressed into a more compact representation that preserves what matters most. By keeping only the components that explain the vast majority of observed variation, the complexity is reduced without erasing the patterns that distinguish organic activity from automation.

<figure class="figure text-center">
  <img src="assets/img/explained_variance.png"
       alt="Cumulative explained variance as a function of the number of principal components"
       style="max-width: 100%; height: auto;">
  <figcaption class="figure-caption">
    <strong>Figure 1.</strong> Cumulative explained variance as a function of the number of principal
    components. The dashed line indicates the 90% variance threshold.
  </figcaption>
</figure>
<br>

Within this simplified space, irregular behavior begins to stand out. Highly automated subreddits tend to follow narrow, repetitive patterns, making them easier to isolate than the messier, more diverse behavior of human communities. Subreddits that repeatedly exhibit these signatures are flagged as bot-heavy and filtered out of the network.

The accompanying visualization highlights the fifteen subreddits with the highest estimated levels of automated activity — the noisiest corners of the platform.

<figure class="figure text-center">
  <img src="assets/img/Top15subreddits.png"
       alt="Top 15 subreddits by bot-like post rate"
       style="max-width: 100%; height: auto;">
  <figcaption class="figure-caption">
    <strong>Figure 2.</strong> Top fifteen subreddits ranked by the proportion of
    posts flagged as bot-like by the Isolation Forest model. 
  </figcaption>
</figure>
<br>

<details class="event-block">
  <summary>
    <span class="event-pill">Why it matters</span>
    <span>Impact of bot filtering on our analysis</span>
  </summary>
  <div>
    <ul>
      <li><strong>Cleaner signals</strong>: Removing bot-heavy subreddits ensures that spikes in activity are driven by human attention, not automated posting scripts.</li>
      <li><strong>More meaningful communities</strong>: Clusters built on filtered data better reflect real social structure instead of artifacts of spam farms or automated link-sharing.</li>
      <li><strong>Stronger event interpretation</strong>: When we later observe changes during major events, we can attribute them to genuine shifts in human behavior rather than background automation.</li>
    </ul>
  </div>
</details>

---

## 3. From Chaos to Communities {#part3}

With bots removed, the Reddit Hyperlink Network is more authentic — but it is still vast, tangled, and nearly impossible to navigate at the level of individual subreddits.

So the perspective shifts.

Instead of focusing on thousands of small communities, hyperlink interactions are grouped into **broader categories of human interest**: politics, sports, gaming, world news, and beyond. At this scale, the network starts to look familiar. Some communities emerge as bridges during moments of intense attention, channeling information across otherwise distant topics. Others remain inward-looking, largely unaffected by external events.

<figure class="flourish-figure">
  <div class="flourish-embed flourish-hierarchy" data-src="visualisation/26914732">
    <script src="https://public.flourish.studio/resources/embed.js"></script>
    <noscript>
      <img src="https://public.flourish.studio/visualisation/26914732/thumbnail"
           width="100%"
           alt="Hierarchy visualization of Reddit communities" />
    </noscript>
  </div>

  <figcaption>
    <strong>Figure 3.</strong> Hierarchical representation of Reddit communities based on hyperlink interactions,
    highlighting the structural organization of clusters across the platform.
  </figcaption>
</figure>

Connections form quickly when the world demands attention, intensify as conversations converge, and then either fade away or settle into more permanent pathways — depending on the nature of the event that sparked them.

---

### A Structure That Suddenly Makes Sense

Seen from a distance, the structure of Reddit snaps into focus. Thousands of subreddits merge into a smaller number of recognizable communities, each reflecting a facet of human curiosity.

This is why, on Reddit, it feels perfectly normal to learn about a new restaurant opening while searching for a gaming tutorial — or to stumble upon a season finale spoiler while trying to figure out how to farm Bitcoin in your basement.

What looks like randomness is, in fact, a network quietly shaped by shared attention.

<figure class="flourish-figure">
  <div class="flourish-embed flourish-network" data-src="visualisation/26916638">
    <script src="https://public.flourish.studio/resources/embed.js">
    </script>
    <noscript>
      <img src="https://public.flourish.studio/visualisation/26916638/thumbnail" width="100%" alt="network visualization" />
    </noscript>
  </div>

  <figcaption>
    <strong>Figure 4.</strong> Network representation of the Hyperlink network.
  </figcaption>
</figure>

<details class="event-block">
  <summary>
    <span class="event-pill">Key idea</span>
    <span>The map we will use for events</span>
  </summary>
  <div>
    <ul>
      <li>The <strong>nodes</strong> of our story are not individual subreddits, but <strong>clusters of related communities</strong>.</li>
      <li>The <strong>edges</strong> are the hyperlinks between them, strengthened or weakened as events unfold.</li>
      <li>This cluster-level map is the backbone for everything that follows: we will watch how it bends, stretches, and sometimes fractures under the pressure of real-world events.</li>
    </ul>
  </div>
</details>

---

<!-- The file is under _includes/intercluster.md -->
<a id="part4"></a>
{% include intercluster.md %}

<!-- The file is under _includes/intra_cluster_analysis.md -->
<a id="part5"></a>
{% include intra_cluster_analysis.md %}

---

## 6. In conclusion {#part6}

The Reddit Hyperlink Network, once examined through rigorous analysis, reveals itself to be far more complex than it first appears. What often feels like a space for absent-minded scrolling — a way to briefly escape the real world — turns out to be a remarkably faithful mirror of it.

Within this network, communities form, evolve, and interact in ways that closely resemble offline social systems. They argue, align, fragment, and occasionally converge around shared moments. World events act as catalysts, pulling attention inward and reshaping how communities relate to one another. Some connections are strengthened through shared focus and collective engagement, while others are strained or weakened as disagreement and emotional intensity rise.

Major events leave the deepest structural footprints. Elections, crises, and globally shared moments reorganize attention at scale, forging links that can persist long after the headlines fade. Yet smaller, more localized events matter too. Even when their impact does not propagate across an entire cluster, they still leave measurable traces within individual communities, briefly redirecting attention and altering internal dynamics.

### What this project reveals about Reddit

- **Reddit behaves like a social system, not just a feed.**  
  Attention moves unevenly, some communities act as bridges, others remain insulated, and a few clusters become central arenas during major events.

- **Shocks reshape structure at multiple scales.**  
  Large-scale events can reorganize whole clusters, while more local shocks like niche game releases or regional crises produce focused but still detectable ripples.

- **The network remembers.**  
  Even after activity settles, the links forged during intense periods — especially around politics and crises — can persist for weeks or months, leaving long-term imprints on how communities interact.

<details class="event-block">
  <summary>
    <span class="event-pill">Big picture</span>
    <span>Reddit as a mirror of the world</span>
  </summary>
  <div>
    <p>
      Across all levels of analysis — between clusters, within clusters, and between specific communities — one pattern remains consistent: Reddit does not react uniformly. Attention spreads asymmetrically, influence depends on context and perceived importance, and engagement is shaped by the same selective pressures that govern real-world interaction.
    </p>
    <p>
      So the next time you follow a hyperlink to another subreddit, pause for a moment before scrolling past. That click may pull you into the center of an unfolding conversation — one that strengthens old ties, challenges existing narratives, or subtly reshapes the structure of a community. In doing so, you become part of the same collective dynamics that quietly turn Reddit into a map of the world it reflects.
    </p>
  </div>
</details>

---

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
