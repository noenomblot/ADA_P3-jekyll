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


### How politics, culture, and social life interact on Reddit

Across dozens of large-scale events between 2014 and 2016, one central insight emerges:  
Reddit reacts strongly to major shocks — but it almost never rewires itself.

Instead of permanently reshaping who talks to whom, events temporarily redistribute
attention, emotion, and intensity along pre-existing community boundaries. Whether
interactions spill across communities depends far more on the *symbolic nature* of
the event than on its objective scale or media coverage.

This section focuses on one core axis of that behavior:  
the relationship between **politics, entertainment, and social life** on Reddit —
and its striking asymmetries.

---

### When politics hits, does culture react? 
Viewed through our three research questions, these results paint a consistent picture: major events do create bursts of cross-community interaction (RQ1), but only a small subset of communities — primarily social and, in rare symbolic cases, humor — act as temporary bridges (RQ2). Crucially, these event-driven ties almost always fade, leaving the long-term structure of the network largely unchanged (RQ3).
**Politics → Entertainment / Movies / TV**

We first examine whether major political shocks pull entertainment communities into
the conversation.

#### Crimea Annexation (2014) — geopolitics without cultural spillover

Despite global media coverage and rising international tension, the annexation of
Crimea remains almost entirely confined to news and geopolitics communities.
Interaction levels with entertainment remain flat, no durable bridges emerge, and
several ties even weaken.

Geopolitical distance matters. When a political event feels remote — geographically
or emotionally — it does not penetrate cultural spaces.

#### Brexit Referendum (2016) — politics enters daily life, but stops short of culture

Brexit represents a clear step forward in spillover. Political discussion expands
outward into social and everyday communities, reflecting how deeply the referendum
affected identity, family, and daily conversation.

However, this expansion remains fragile. While interaction intensity rises
temporarily, no long-term cultural bridges form. Entertainment communities remain
largely untouched. Politics becomes personal — but not cultural.

#### US Presidential Election (2016) — maximum polarization, minimal rewiring

The election of Donald Trump generates the strongest emotional response in the
dataset. Sentiment polarizes sharply, existing ties are used more intensely, and
social communities absorb political debate at scale.

Yet even here, the structure holds. Political interaction does not expand durably
into entertainment communities. The same bridges are reused — none are newly built.
Politics amplifies emotion, not structure.

#### Politics → Entertainment: what we learn

Across all three political events:

- Politics sometimes spills into social spaces  
- Politics rarely spills into entertainment  
- Politics never durably rewires cultural communities  

Entertainment remains structurally insulated from political shocks.

---

### Does culture ever pull politics in?  
**Entertainment → Politics**

To test the reverse direction, we analyze three of the largest cultural events of the
period.

#### Star Wars: *The Force Awakens* (2015) — massive attention, zero political pull

Despite being one of the biggest cultural releases of the decade, *Star Wars*
produces no increase in political interaction. Political communities remain
structurally unchanged — if anything, interaction slightly declines.

Popularity alone is not enough.

#### Oscars 2016 (*#OscarsSoWhite*) — culture brushes politics, briefly

Unlike *Star Wars*, the Oscars explicitly intersect with political themes: diversity,
representation, and inequality. Here, we observe a short-lived increase in
interaction between entertainment and politics.

But the effect does not stabilize. No new bridges form, correlations return to
baseline, and the network quickly relaxes. Culture can open political conversations —
but it does not reorganize them.

#### Game of Thrones, Season 6 (2016) — culture rewires itself, not politics

The Season 6 premiere of *Game of Thrones* creates one of the strongest internal
cultural reconfigurations in the dataset. New entertainment-to-entertainment ties
emerge and persist.

Yet political interaction declines. As culture intensifies, politics fades into the
background. Entertainment pulls inward, not outward.

#### Entertainment → Politics: a clear asymmetry

Across all entertainment events:

- No lasting political spillover  
- No new political bridges  
- Political communities remain structurally insulated  

Politics can leak into culture — but culture does not flow back into politics.

Notably, even when entertainment events are explicitly politicized (e.g.
*#OscarsSoWhite*), they fail to generate durable political spillover. Politicization
alone is insufficient without identity-level conflict.

---

### Social communities: where politics actually lands

While entertainment remains insulated, social communities behave very differently.
A clear gradient of political spillover emerges:

- Crimea → minimal social impact  
- Brexit → partial, unstable spillover  
- Trump election → strong and significant social embedding  

When politics touches identity, legitimacy, and everyday norms, social communities
become central arenas of debate. Yet even here, Reddit’s structure resists permanent
change:

- Existing ties intensify  
- Emotions surge  
- The architecture remains intact  

---

### Terrorism vs. health: symbolism matters more than severity

#### Charlie Hebdo (2015) — politics becomes social

Because the attack directly targeted expression and satire, political discourse
spills powerfully into both social and humor communities. Interaction increases are
strong and statistically significant. Politics becomes a symbolic social movement.

#### Paris Attacks (2015) — emotion without structural change

The November attacks trigger intense emotional reactions, but no lasting political
embedding in social spaces. Grief and solidarity surge — structure does not shift.

#### Ebola (2014) — fear without diffusion

Ebola generates fear, but no political or social spillover. Health discussion
contracts inward, remaining technical and informational. Severity alone is not
enough; symbolism is decisive.

---

### Sports, gaming, and collective attention

Outside politics, other domains reveal the same structural logic:

- Sports events strongly activate social interaction — but never permanently rewire it  
- Gaming spills into social space only when it alters offline behavior (e.g. Pokémon GO)  
- Technology launches remain socially insulated unless they create collective participation  

Across all cases, attention synchronizes communities — structure resists change.

---

### Final takeaway

Across politics, culture, social life, sports, gaming, and health, Reddit follows a
consistent rule:

**Major events change how Reddit talks — not who talks to whom.**

Political shocks amplify emotion and sometimes spill into social spaces.  
Cultural shocks reorganize culture internally but leave politics untouched.  
Health crises concentrate discussion without diffusion.  
Social communities absorb identity-driven conflict — but temporarily.

Reddit reacts.  
Reddit adapts.  
But Reddit almost never rewires.


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

