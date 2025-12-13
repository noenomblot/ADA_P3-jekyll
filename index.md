---
layout: page
title: "Reddit Rewired: Event-Driven Bridges"
subtitle: How global events reshape (or fail to reshape) Reddit communities
cover-img: /assets/img/reddit_header.png
---

## Introduction

Reddit is made of thousands of communities (“subreddits”) that usually live in their own bubbles.  
Most of the time, people post and comment inside a single subreddit, reinforcing the same topics, norms, and viewpoints.

But what happens when **the world shakes**?

- A presidential election.  
- A blockbuster release.  
- A global crisis.

Do these events:

- create **new links** between communities that usually never talk to each other?  
- turn some subreddits into temporary **“bridges”**?  
- leave **long-term scars** in the network, or do things quickly go back to “normal”?

In this data story, we will explore these questions using the **Reddit Socio-Reddit Hyperlinks dataset**, and additional information about real-world events.

We structure the story around three main research questions:

- **RQ1 – Do big events trigger bursts of new links between communities that usually barely connect?**  
- **RQ2 – Which communities act as early signalers or temporary bridges during these events?**  
- **RQ3 – Do these event-driven ties disappear quickly, or do some become part of the long-term backbone of the network?**  

> 🔎 *All the graphs you see below come from a previous ADA project about movies and diversity.  
> We temporarily keep them as **examples of how to embed figures** in the website.  
> They will be progressively replaced with our own Reddit plots as our analysis evolves.*

{: .text-justify}

<p align="center">
    <img src="assets/img/great_success.jpg" alt="" width="300"/> <!-- Example image kept from previous project -->
</p>

---

## 1. From Hyperlinks to Communities

In the final version, this section will:

- explain how we build the **Reddit hyperlink network**:
  - each node = a subreddit  
  - each edge = a hyperlink from a post in subreddit A pointing to subreddit B
- show basic **descriptive statistics**:
  - number of posts, subreddits, edges  
  - degree distribution, top “hub” communities
- describe our **preprocessing**:
  - how we handle bots / spammy subreddits  
  - how we aggregate edges over time (per day/week)
- introduce our **community detection**:
  - which algorithm we use (e.g. Louvain)  
  - how we interpret the main clusters (politics, movies, gaming, etc.)

Below, we keep a few blocks from the previous project as layout examples.

### Example: Dataset Description Block

<div style="display: flex; align-items: center; justify-content: center;">
    <!-- Left Side: Image -->
    <div style="margin-right: 20px;">
        <img src="assets/img/video_camera.png" alt="" style="max-width: 150px; height: auto;">
    </div>
    
    <!-- Right Side: Text -->
    <div>
        <b>Example dataset description from a previous project:</b>
        <ul>
            <li>Movie Name</li>
            <li>Release Year</li>
            <li>Actor Ethnicity</li>
            <li>Box Office Revenue</li>
        </ul>
        <i>We will later replace this with a similar bullet list describing our Reddit hyperlink dataset (columns, time range, etc.).</i>
    </div>
</div>


<div style="display: flex; align-items: center; justify-content: center;">
    <!-- Left Side: Text -->
    <div style="margin-right: 20px;">
        <b>Example of enriched datasets:</b>
        <ul>
            <li>IMDb datasets and ratings.</li>
            <li>Awards and nominations.</li>
            <li>Mapping between different ID systems.</li>
        </ul>
        <i>In our project, this block will describe external data we add (event lists, Google Trends, etc.).</i>
    </div>
    
    <!-- Right Side: Image -->
    <div>
        <img src="assets/img/oscar.png" alt="" style="max-width: 150px; height: auto;">
    </div>
</div>

<div style="text-align: center; font-size: 20%; line-height: 1; display: inline-block;">
    {% include distribution_realease_date.html %}
</div>

*Example figure from the previous project showing movie release dates.  
We will later replace this with a plot of our own (e.g., distribution of hyperlinks per day or per year).*

{: .text-justify}

---

## 2. Event-Born Links: Short Flares or Lasting Imprints?

Here we will focus on **RQ1 and RQ3**:

- How many **new edges** between communities appear during major events?  
- Do these edges connect communities that were almost disconnected before?  
- Once the event is over, how fast do these edges **disappear**?  
- For edges that survive, do they become part of a new “baseline” interaction?

Planned content (to be filled once analyses are ready):

- define what we call an **“event-born edge”**  
- compare event vs non-event periods  
- build simple **survival curves** for edge persistence  
- discuss which types of events create longer-lasting ties.

### Example: Old Ethnicity Plots (Kept for Layout)

<p align="center">
<img src="assets/img/Intouchable.gif" alt=""/>
</p>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include ethnicities_piechart.html %}
</div>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include ethnic_groups_piechart.html %}
</div>

*Later, we might reuse this layout to show how subreddits are grouped into clusters (politics, movies, etc.).*

---

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include diversity_histogram_essai.html %}
</div>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include average_diversity_per_year.html %}
</div>

*Example histogram + time series layout that we will reuse with our own Reddit metrics.*

---

## 3. Example Highlight Box (To Reuse)

The “Movie Success Criteria” block below is a nice visual element that we plan to reuse.  
We will adapt the text later, for example to define:

- our **event windows** (pre / during / post)  
- or what counts as a **“new cross-link”** and as a **“persistent tie”**.

For now, we keep it as an example:

{% include ingredients_of_success.html %}

---

## 4. Zooming into Events and Communities (Template)

In the final story, this section will be the core of **RQ2**:

- Identify which communities act as **bridges** during events.
- Compare how different types of communities react:
  - e.g. political vs cinema clusters.
- Look at a detailed **case study**:
  - e.g. US election and the behaviour of key political subreddits.

Planned structure:

1. **Global view** – how activity changes around events.  
2. **Politics vs Cinema** – two worlds reacting differently.  
3. **Inside a political cluster** – who talks to whom during the US election?  

Below, we keep some of last year’s plots purely as layout templates (group comparisons, side-by-side figures, etc.).

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include diversity_success.html %}
</div>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include t_test_Overall_success.html %}
</div>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include corr_Success_Spearman.html %}
</div>

*Later, these layouts can host comparisons such as “event vs non-event”, “bridge communities vs others”, etc.*

---

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include diversity_box_office.html %}
</div>

<div style="display: flex; justify-content: space-around; align-items: flex-start; gap: 20px;">
    <div style="text-align: center; font-size: 80%; line-height: 1.2;">
        {% include t_test_Box_office_revenue.html %}
    </div>

    <div style="text-align: center; font-size: 80%; line-height: 1.2;">
        {% include corr_Movie_box_office_revenue_Pearson.html %}
    </div>
</div>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include diversity_ratings.html %}
</div>

<div style="display: flex; justify-content: space-around; align-items: flex-start; gap: 20px;">
    <div style="text-align: center; font-size: 80%; line-height: 1.2;">
        {% include t_test_Ratings.html %}
    </div>

    <div style="text-align: center; font-size: 80%; line-height: 1.2;">
        {% include corr_Ratings_Pearson.html %}
    </div>
</div>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include propensity_score_matching_ratings.html %}
</div>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include diversity_nominations.html %}
</div>

<div style="display: flex; justify-content: space-around; align-items: flex-start; gap: 20px;">
    <div style="text-align: center; font-size: 80%; line-height: 1.2;">
        {% include t_test_Nomination.html %}
    </div>

    <div style="text-align: center; font-size: 80%; line-height: 1.2%;">
        {% include corr_Nomination_Spearman.html %}
    </div>
</div>

---

## 5. What This Means for Echo Chambers (Conclusion Template)

<p align="center">
<img src="assets/img/omar_sy_triste.gif" alt=""/>
</p>

In the final story, this conclusion will:

- summarise our main findings:
  - how often events create only short-lived bridges,  
  - which communities act as repeat “bridges”,  
  - which event-born ties seem to become structural.
- discuss what this means for **echo chambers** and information flow on Reddit.  
- reflect on the **limitations**:
  - one dataset, one time period  
  - hyperlink-based interactions only  
  - possible biases in event selection.

For now, we keep it as a template and will fill it once analyses are complete.

{: .text-justify}

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

