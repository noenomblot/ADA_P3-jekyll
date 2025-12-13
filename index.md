---
layout: page
title: "Reddit Rewired: Event-Driven Bridges"
subtitle: How global events reshape (or fail to reshape) Reddit communities
cover-img: /assets/img/header_img.png
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
- turn some subreddits into **temporary “bridges”**?
- leave **long-term scars** in the network, or do things quickly go back to “normal”?

In this data story, we will explore these questions using the **Reddit Socio-Reddit Hyperlinks dataset**, and additional information about real-world events.

We will structure the story around three main research questions:

- **RQ1 – Do big events trigger bursts of new links between communities that usually barely connect?**  
- **RQ2 – Which communities act as early signalers or temporary bridges during these events?**  
- **RQ3 – Do these event-driven ties disappear quickly, or do some become part of the long-term backbone of the network?**  

> 🔎 **Note:** all the plots you see below (histograms, pie charts, correlation plots, etc.) come from a *previous* ADA project about movies and diversity.  
> We temporarily keep them as **examples of how to embed graphs** in the website.  
> They will be progressively replaced with our own figures as our analysis evolves.

{: .text-justify}

<p align="center">
    <img src="assets/img/great_success.jpg" alt="" width="300"/> <!-- Example image kept from previous project -->
</p>

---

## 1. From Hyperlinks to Communities

In our final version, this section will:

- explain how we build the **Reddit hyperlink network**:
  - each node = a subreddit,
  - each edge = a hyperlink from a post in subreddit A pointing to subreddit B.
- show basic **descriptive statistics**:
  - number of posts, number of subreddits, number of edges,
  - degree distribution (which subreddits are the biggest “hubs”?).
- describe our **preprocessing choices**:
  - how we handle bots and spammy subreddits,
  - how we deal with time (aggregating links per day / per week).
- introduce the **community detection**:
  - which method we use (e.g. Louvain),
  - how we interpret the main clusters (politics, movies, gaming, etc.).

Below, we keep some of last year’s content as **layout examples**.

### Example: How to Present Datasets

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
        <i>We will replace this with a similar bullet list describing our Reddit hyperlink dataset (columns, time range, etc.).</i>
    </div>
</div>


<div style="display: flex; align-items: center; justify-content: center;">
    <!-- Left Side: Text -->
    <div style="margin-right: 20px;">
        <b>Example of enriched datasets:</b>
        <ul>
            <li>IMDb ratings and titles.</li>
            <li>Awards and nominations.</li>
            <li>Mappings between different ID systems.</li>
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

### 1.1 Our Research Questions (Template)

In the actual version of the story, this section will:

- recap our three research questions in a visual / friendly way,
- give the reader an intuition of:
  - what a “cross-link” between communities means,
  - why events might create temporary bridges,
  - what it would mean for a tie to “persist” after the event.

For now, we keep this as a **placeholder** and will enrich it once all results are finalized.

---

## 2. Event-Born Links: Short Flares or Lasting Imprints?

In this part of the story, we want to focus on **RQ1 and RQ3**:

- How many **new edges** between communities appear during major events?
- Are these edges connecting communities that were almost disconnected before?
- Once the event is over, how fast do these edges **disappear**?
- For edges that survive, do they become part of a new “baseline” interaction?

Concretely, we plan to:

- label edges that are **“born” during an event window**,
- track whether the same subreddit pairs interact again after:
  - 7 days, 30 days, 90 days, etc. (simple survival curves),
- compare:
  - edges born during events vs edges born in “normal” periods,
- summarize everything into:
  - a few **intuitive plots** (barplots, survival curves),
  - and **simple takeaways** (e.g. “Most event-born ties vanish quickly, but a small fraction become stable.”).

Below, we keep two example pie charts from the previous project to remember how to embed such figures.

### Example: Grouping Categories (Old Ethnicity Plots)

<p align="center">
<img src="assets/img/Intouchable.gif" alt=""/>
</p>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include ethnicities_piechart.html %}
</div>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include ethnic_groups_piechart.html %}
</div>

*These two pie charts were used to show how ethnicities were grouped into larger categories.  
Later, we might use similar plots to show how subreddits are grouped into communities (clusters) in our network.*

---

### Example: Distribution and Evolution of a Score

In the previous project, this section introduced a **diversity score** and its evolution over time.

In our case, this is where we will:

- define a **simple metric** related to event-born edges, for example:
  - fraction of edges that connect previously unconnected communities,
  - or an “event novelty index” for each event.
- show how this metric is distributed across events,
- highlight a few particularly interesting cases (very high / very low novelty).

Below, we keep the original figures as examples of:

- histogram layout,
- time series layout.

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include diversity_histogram_essai.html %}
</div>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include average_diversity_per_year.html %}
</div>

---

## 3. Example Section: Styled Highlight Box (To Reuse)

The “Movie Success Criteria” block below is a **nice visual element** from the previous project.  
We keep it as an example of:

- how to highlight an important definition,
- how to break the text flow with a colored box.

Later, we can reuse this exact layout for something like:

- **“Event Window Definitions”** (pre-event / during / post-event),
- or **“What we call a ‘new cross-link’”**,
- or **“How we define long-term persistence”**.

For now, we simply keep the include:

{% include ingredients_of_success.html %}

---

## 4. Zooming into Events and Communities

This big section will eventually correspond to:

- **RQ2 (bridges / early signalers)**,
- and the more detailed event-level analysis.

We plan to split it into three main parts:

1. **Overall network patterns**
   - How does global edge activity change around events?
   - Do we see bursts of cross-community edges?
2. **Zoom by community type (e.g. politics vs cinema)**
   - A political event vs a cinema event:
     - which clusters react more strongly,
     - how cross-links behave in each case.
3. **Deep dive into a political cluster**
   - Focus on a specific cluster (e.g. US politics),
   - track who talks to whom before / during / after a key event,
   - identify subreddits that become **temporary bridges**.

Pour ne pas perdre les exemples de graphs, on garde quelques blocs de la section “The Truth of Data” comme **gabarits**. Chaque sous-partie ci-dessous est un exemple de visualization qu’on pourra adapter.

### 4.1 Overall Patterns (Template)

*In the final version, this part will:*

- compare **event days vs normal days** in terms of:
  - number of edges,
  - number of cross-community edges,
  - number of “first-time” edges between community pairs.
- possibly use:
  - boxplots or barplots to compare distributions,
  - simple statistical tests (t-tests or non-parametric tests),
  - small text explaining whether the differences are large or small.

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include diversity_success.html %}
</div>

*Example layout from last year’s project (successful vs unsuccessful movies).  
We will replace this with a comparison of “event vs non-event” periods.*

---

### 4.2 Example: Group Comparison + Test

Below are examples of how to present:

- a **difference of means** (t-test),
- and a **correlation plot**.

In our story, similar layouts could be used to show:

- whether “event-born edges” differ significantly from “normal edges”,
- or whether some event-level metric is correlated with network outcomes.

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include t_test_Overall_success.html %}
</div>

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include corr_Success_Spearman.html %}
</div>

---

### 4.3 Template for More Detailed Criteria

The following subsections (Box Office, Ratings, Nominations) come from the cinema project.  
We keep them as **structural templates** to remind ourselves how to:

- split a long analysis into several sub-criteria,
- show one or two plots side-by-side,
- combine text + graph in a readable way.

In our Reddit project, the equivalents could be:

- 4.3.1 Cross-links volume per community type  
- 4.3.2 Sentiment or polarity of cross-links  
- 4.3.3 Persistence of ties after the event

#### <span class="criteria-icon">💰</span> Example layout: “Box Office” section

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

*We will later reuse this structure for one of our own event-related comparisons (e.g. strong vs weak events, or high vs low persistence).*

#### <span class="criteria-icon">⭐</span> Example layout: “Ratings” section

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

#### <span class="criteria-icon">🏆</span> Example layout: “Nominations” section

<div style="text-align: center; font-size: 80%; line-height: 1.2;">
    {% include diversity_nominations.html %}
</div>

<div style="display: flex; justify-content: space-around; align-items: flex-start; gap: 20px;">
    <div style="text-align: center; font-size: 80%; line-height: 1.2;">
        {% include t_test_Nomination.html %}
    </div>

    <div style="text-align: center; font-size: 80%; line-height: 1.2;">
        {% include corr_Nomination_Spearman.html %}
    </div>
</div>

---

## 5. What This Means for Echo Chambers (Conclusion Template)

<p align="center">
<img src="assets/img/omar_sy_triste.gif" alt=""/>
</p>

In the final version of the project, this conclusion section will:

- summarize our key findings, for example:
  - “Big events create many short-lived bridges, but only a small fraction of ties persist.”
  - “Certain communities systematically act as bridges across clusters.”
  - “Some event-driven ties become part of the long-term backbone of Reddit.”
- discuss what this means for:
  - **echo chambers**,
  - information diffusion,
  - the role of “bridge communities” during crises.
- reflect on the limitations:
  - only one dataset, one time range,
  - only hyperlink-based interactions,
  - possible biases in the events we select.

For now, we keep this as a **template** and will fill it once all analyses are complete.

{: .text-justify}

---

## References

<ul>
    <li>
        <i>Example reference from previous project:</i><br>
        <a href="https://socialsciences.ucla.edu/wp-content/uploads/2024/06/UCLA-Hollywood-Diversity-Report-2024-Film-Streaming-5-23-2024.pdf" target="_blank">
            UCLA Social Sciences. <i>Hollywood Diversity Report 2024: Film and Streaming</i>.
        </a><br>
        <i>We will replace this list with our own references (papers on Reddit, event networks, etc.).</i>
    </li>
</ul>
