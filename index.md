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



### When the world sneezes, Reddit catches a cold

When a major world event occurs — an election night, a surprise product launch, or a
breaking news story — millions of people turn to the internet to discuss, debate,
explain, and react. With its thousands of semi-independent communities, Reddit
becomes a dynamic map of collective attention.

But how does this attention actually move? Do communities that usually ignore one
another suddenly interact? And once the moment passes, do these connections fade
away, or do they leave a lasting trace?

This project approaches Reddit not as a collection of isolated subreddits, but as a
dynamic network whose structure bends and responds to real-world events. By
tracking hyperlinks between subreddits over time, we observe how information flows,
which communities act as temporary bridges, and whether event-driven interactions
become part of Reddit’s long-term backbone or disappear as quickly as they emerge.

Using a large-scale hyperlink dataset enriched with sentiment measures, subreddit
embeddings, and external timelines of world events, we zoom in on moments of
collective attention and ask a simple question with complex implications: when the
world changes, does Reddit reorganize itself?

In the sections that follow, we move from global patterns to local interactions —
tracking bursts of connectivity, identifying short-lived brokers of information,
and measuring the persistence of relationships formed under the pressure of major
events. What emerges is a portrait of online communities that are highly reactive
yet structurally resilient, revealing how digital spaces mirror — and sometimes
amplify — the rhythms of the real world.


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

## Part 2: Adapting the data

On online discussion platforms such as Reddit, automated accounts (“bots”) can
substantially influence information dynamics by amplifying specific topics,
spreading misinformation, or artificially sustaining conversations. Identifying
and filtering these accounts is therefore a critical preprocessing step before
any network analysis, as bot activity can distort link structures and bias both
clustering and sentiment results.

To detect bot-like behavior, we rely on unsupervised anomaly detection methods, as
no labeled ground truth is available. We exploit the textual, behavioral, and
sentiment features provided in the dataset, resulting in an initial set of 85
features per subreddit.

Our approach combines two main techniques. First, we apply Principal Component
Analysis (PCA) to reduce the dimensionality of the feature space while preserving
most of its informational content. We retain 90% of the total variance, which is
captured by 48 principal components. This step limits noise and redundancy while
maintaining the dominant behavioral patterns.

Second, we use an Isolation Forest model on the reduced feature space to identify
abnormal activity patterns consistent with automated behavior. The resulting
scores allow us to estimate the relative prevalence of bot-like activity across
subreddits. The figure below presents the fifteen subreddits with the highest
estimated bot-post rates according to this model.

From a network-analysis perspective, filtering out subreddits with extreme bot
activity is essential. Our objective is to model Reddit as a social information
network driven by human interactions, where edges represent meaningful exchanges
between communities. High levels of automation would otherwise introduce spurious
links and artificially inflate connectivity.

In parallel, our early analyses of event-driven effects at the global network
level revealed a classical case of Simpson’s paradox: trends observed within
specific subgroups disappeared or reversed when aggregating the entire network.
This observation reinforced the need for clustering the network prior to
interpretation.

The clustered network presented here highlights the fourteen most connected
clusters among the twenty identified across Reddit. Even at this coarse level,
clear structural patterns emerge. Some clusters act as hubs, connecting a wide
range of communities, while others remain more peripheral with narrower, topic-
focused interactions.

In the sections that follow, we build on this clustered representation to examine
how information flows across Reddit and how different types of communities respond
to major real-world events.


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

Major real-world events often trigger visible surges of activity on Reddit.
But do they actually reshape how communities connect to each other — or do they
merely amplify existing pathways?

To answer this question, we focus on **inter-cluster relationships**, tracking how
links between major thematic communities evolve *before*, *during*, and *after*
key global events.

---
We define an event-born edge as an inter-cluster hyperlink that appears for the first time during the event window and was absent in a matched pre-event baseline.

### Political shocks: strong spillovers, no structural creation

#### US Presidential Election (2016) — Political Shock

The 2016 US presidential election represents the most intense political shock in
our dataset. On Reddit, political discussion spills decisively into social and
relational communities.

Interactions between Politics / News and Social clusters increase sharply and
remain elevated well beyond the event window. Several existing inter-cluster ties
strengthen substantially, and sentiment shifts are pronounced, both positively
and negatively.

Yet despite this intensity, the underlying network structure remains unchanged.
No new inter-cluster relationships emerge, and no lasting structural bridges are
created. The same pathways are reused more intensively, but no new ones are added.

This pattern highlights a key distinction: high impact does not necessarily imply
structural novelty.

#### Charlie Hebdo Attacks (2015) — Political Crisis

The Charlie Hebdo attacks generate a different kind of political shock — one that
directly targets satire, free expression, and cultural identity.

Here, interactions between Politics / News and Humor / Reddit, as well as broader
cultural clusters, intensify strongly. A wide range of existing inter-cluster ties
strengthen simultaneously, reflecting collective emotional processing across
diverse communities.

Once again, however, no new inter-cluster relationships appear. The event amplifies
communication across many existing channels, but does not produce new long-term
structural connections.

Political crises, even when emotionally charged and culturally symbolic, appear to
activate the network without rewiring it.

---

### Collective entertainment: broad engagement, limited persistence

#### Super Bowl XLIX (2015) — Global Sports Event

The Super Bowl produces a short-lived but widespread social response. Sports
discussions spill into general, social, and entertainment-related clusters, with
many existing inter-cluster ties strengthening temporarily.

The persistence of these effects is moderate: interaction levels remain somewhat
elevated after the event, but gradually return toward baseline. No new inter-cluster
relationships are created, and weakened ties re-emerge shortly after.

This suggests that shared cultural spectacles mobilize attention broadly, but
rarely leave lasting structural traces.

#### Pokémon GO Launch (2016) — Cultural Phenomenon

The launch of *Pokémon GO* generates one of the most diffuse engagement patterns in
the dataset. Gaming communities connect more intensely with Social, General, and
Technology-related clusters, reflecting the game’s broad demographic reach.

Despite this unusually wide spillover, the pattern remains consistent with
previous cases: existing inter-cluster ties strengthen, sentiment shifts slightly,
but no new structural links emerge. The network absorbs the shock through
amplification rather than expansion.

---

### A consistent pattern: amplification without rewiring

Across political crises, cultural tragedies, and mass entertainment events, a
striking regularity emerges:

- No event creates new inter-cluster relationships at the structural level  
- Events consistently strengthen pre-existing bridges between communities  
- These effects are often partially lasting, but do not redefine the long-term
  backbone of the network  

In other words, Reddit reacts strongly — but conservatively. The network flexes
under pressure, channels attention through established pathways, and then
stabilizes without forming new durable connections.

---
### Cluster-level sentiment dynamics

While event-driven structural changes are extremely rare, sentiment reacts strongly
to major events — but in a highly non-uniform way across communities. Importantly,
the clusters experiencing the largest sentiment shifts are not the clusters where
events originate. Political, entertainment, and gaming communities primarily act as
sources of information and attention, rather than as sites of peak emotional
expression.

Instead, the strongest sentiment gains consistently appear in peripheral or
low-constraint clusters such as NSFW, Food, Finance, Humor / Reddit, and General.
These communities are loosely tied to specific topics and allow more expressive,
informal, or affective discourse. Across political crises, cultural shocks, and
entertainment releases, they function as emotional spillover zones, absorbing
reactions that remain weakly expressed in event-specific clusters.

This displacement of sentiment helps explain the network’s structural resilience.
Emotional intensity is redistributed away from tightly organized communities,
preventing local overload and reducing the incentive for new structural connections
to form. In this sense, sentiment diffuses broadly while structure remains
conservative: Reddit processes emotion through redirection rather than rewiring.
---
### What this tells us about event-driven connectivity

These findings suggest that Reddit’s community structure is highly resilient.
Even moments of shared global attention rarely create genuinely new links between
distant communities. Instead, events activate and intensify latent connections
that already exist.

This raises an important question for the remainder of the analysis:
**Are there any events that truly break this pattern?**

#### Game of Thrones, Season 6 (2016) — when fiction creates new bridges

The release of *Game of Thrones* Season 6 marks a rare departure from Reddit’s usual
structural stability.

Unlike political crises or mass sporting events, the premiere generates twelve
entirely new inter-cluster relationships between Entertainment / Movies / TV and
Politics / News communities. These links are absent in the two months preceding the
event and persist beyond the immediate post-event window.

This indicates genuine structural novelty: for once, a global cultural event does
not merely amplify existing pathways — it creates new ones.

The persistence of these connections is nonetheless nuanced. While the new links
remain present in the network, their interaction intensity declines rapidly after
the event. The overall persistence score reflects this dynamic: the structure
survives, but the activity does not.

This pattern contrasts sharply with political shocks such as the 2016 US
presidential election, where interaction surges dramatically but no new structural
connections emerge.

Taken together, these cases reveal a key asymmetry: fictional universes can
temporarily rewire the network, whereas political crises primarily reuse existing
bridges.

#### Not all cultural blockbusters rewire the network  
*Star Wars: The Force Awakens* (2015)

Despite its global reach and massive online engagement, the release of *Star Wars:
The Force Awakens* does not produce meaningful structural reconfiguration of the
Reddit network. Existing connections between entertainment communities and the
broader Reddit ecosystem are activated and sometimes intensified, but no new
inter-cluster relationships emerge that alter the long-term architecture.

This contrast highlights an important distinction: scale alone is insufficient to
rewire the network. While *Game of Thrones* Season 6 introduces genuinely new
connections across communities, *Star Wars* primarily mobilizes pre-existing
fandom structures.

Taken together, these cases suggest that narrative discontinuity and episodic
anticipation — rather than sheer popularity — are key drivers of structural
novelty in event-driven connectivity.



<!-- The file is under _includes/intra_cluster_analysis.md -->
{% include intra_cluster_analysis.md %}





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
## 6. Graphs from previous project
Below, we keep a few blocks from the previous project as layout examples.
> 🔎 *All the graphs you see below come from a previous ADA project about movies and diversity.  
> We temporarily keep them as **examples of how to embed figures** in the website.  
> They will be progressively replaced with our own Reddit plots as our analysis evolves.*

{: .text-justify}

<p align="center">
    <img src="assets/img/great_success.jpg" alt="" width="300"/> <!-- Example image kept from previous project -->
</p>

---
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

