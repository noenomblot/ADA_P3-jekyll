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


## 3. Zooming into Events and Communities (Template)

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

In the politics/news cluster, the biggest subreddits in terms of subreddit interactions are unsurprisingly political. The biggest being "the_donald" a right wing (now banned) subreddit supporting Donald Trump especially during the 2016 US presidential election. The second biggest is "conspiracy" and the third and fourth "politics" and "news", two subreddits also strongly involved in the US election cycle of 2016. It has to be noted that "politics" and "news" tend to be anti-Trump and are taken as "the_donald"s counter-pole in our analysis.

<figure id="fig-plot-top-subreddits-politics">
  <div class="plotly-embed-smaller">
    <iframe
      src="{{ 'assets/img/plots/top-subreddit-interaction-politics.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Top subreddits in the politics/news cluster.
  </figcaption>
</figure>

The temporal graph in [figure ???](#fig-normalized-weekly-politics) clearly shows how important the US elections were in the discussions. Towards the elections on November 8th 2016, the hyperlinks increase continuously and then beginning of December they suddenly fall. Interesting also is the peak in October 2015, but we where unable to find any event related reason why a peak would happen at that time.


<figure id="fig-normalized-weekly-politics">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/plots/normalized_weekly_politics.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Hyperlink activities over time in the politics/news cluster.
  </figcaption>
</figure>

In [figure ???](#fig-sliding-event-intensity) the sliding event intensity is shown. For this graph, the absolute number of hyperlinks was averaged inside a timeframe of 3 days to show the the local trends without taking into account the constant rising in post numbers. What really comes apparent are two things: The first is that with increasing number of hyperlinks, the variation in number of posts becomes more erratic. This may be due to a fast reaction of the subreddits on events, but it could also be due to increasing numbers of multiple link targets in one post as more posts with links happen overall. 

The second thing to note is the intensity of the "post-election" collapse in link numbers. Even when averaging the surrounding days, the intensity falls significantly and permanently. The existence of this depression supports the thesis that the erratic-ness of the post intensity is due to world events, as after the major world event, the erratic-ness decreases as well.

<figure id="fig-sliding-event-intensity">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/plots/sliding_event_intensity_politics.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Sliding event intensity in the politics/news cluster.
  </figcaption>
</figure>

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
social communities absorb political debate at scale. As shown in [Figure ???](#fig-cluster-graph-US-election), in the time period around the US election, everything is about Donald Trump or the election. In the figure, the subreddits "the_donald" and "hillaryclinton" are highlighted and it can clearly be seen how dominating they, and especially "the_donald" and their close neighbors, are.


<figure id="fig-cluster-graph-US-election">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/clusters/temporal_cluster_graph_US_election.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Daily hyperlink activities around the US election.
  </figcaption>
</figure>


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

<figure id="fig-plot-normalized-weekly-entertainment">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/plots/normalized_weekly_Entertainment.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Weekly activity in the Entertainment subreddit.
  </figcaption>
</figure>

The daily activity in the cluster predictably increases over time if only due to increased size of reddit itself. The analysis shows some strong peaks, though we were unable to relate them to a specific event.

Analyzing the top communities in the entertainment cluster, we can notice most of them are generalist or humorist subreddits which cover a whole branch of media. The first non-generalist subreddit is "pokemongivaway", though being a giveaway subreddit it is heavily skewed towards linking and being linked to. The second interesting one is "starwars" and as it is, there was a huge blockbuster release in 2015, so inside the period of our dataset.

<figure id="fig-plot-top-subreddits-entertainment">
  <div class="plotly-embed-smaller">
    <iframe
      src="{{ 'assets/img/plots/top-subreddit-interaction-entertainment.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Top subreddits in the entertainment cluster by number of interactions.
  </figcaption>
</figure>

#### Star Wars: *The Force Awakens* (2015) — massive attention, zero political pull

[Figure ???](#fig-cluster-graph-force-awakens) shows the temporal graph around the release of *The Force Awakens* on December 18, 2015, the first film of the so called "sequel-trilogy". We see many hyperlinks leading to or away from the main star wars subreddit "starwars", but this effect is only visible for a few days after the film's release.

<figure id="fig-cluster-graph-force-awakens">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/clusters/temporal_cluster_graph_force_awakens.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Daily hyperlink activities around release of the film "The Force Awakens".
  </figcaption>
</figure>

Despite the seemingly visual increase in activity that day, we cannot confirm any significant or lasting effect following on the whole cluster following the film's release. However what we are able to tell is that in the ego-network of the subreddit "starwars", the ties to a subreddit called "starwarsspeculation" got strengthened. This makes sense, as a new film in a long series always leads to new and exciting speculations by fans on what future movie instances in the star wars universe bring forth.

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
emerge and persist. The short term effect can clearly be seen in [Figure ???](#fig-cluster-graph-gameofthrones), which shows markedly more hyperlink connections after the 24th of April, the date of the episode release. The persisting hyperlink frequency compared to *The Force Awakens* release is likely also due to the continual nature of the serial format.

<figure id="fig-cluster-graph-gameofthrones">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/clusters/temporal_cluster_graph_gameofthrones.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Daily hyperlink activities around release the first episode of season 6 of Game of Thrones.
  </figcaption>
</figure>

It is hard to conclusively tell if there is really lasting change in the subreddit structure, though there seems to be a slight increase in subreddit activity at the event, which could translate into a lasting change after.

It is also interesting to look at the relation between the two main *Game of Thrones* themed subreddits: "freefolk" and "gameofthrones". Our statistical analysis shows a slight increase in lasting subreddit relations in the weeks after the release of the first episode. The Cohen's d-test shows a value of 0.484 which is a moderate increase in activity, though with a p value of 0.16, we cannot conclude the effect being due to the episode's release.

Now the logical follow up question would be to see the values after the release of the last of season 6's episodes on June 26th, and indeed, we a decay in activity between the two subreddits. This decay however is quite a bit smaller, for Cohen's d being -0.374 and here we can clearly reject the hypothesis of the last episode of the season causing a break of previously forged bonds between "freefolk" and "gameofthrones", because our p-value proving it is 0.75, 

We cannot conclusively confirm if season 6 of the series *Game of Thrones* really lead to increased cluster activity and lasting relationships between two of the series main subreddits, but we can tentatively say it lead to an increase in their bonds and clearly state there is no discernable decrease after the season ended.


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
spills powerfully into both social and humor communities. 

In [Figure ???](#fig-cluster-graph-charlie-hebdo) we can see a visual increase of hyperlinks on the highlighted "paris" and "france" subreddits, though this increase is not much stronger. There is also an increase in links from "france" towards arabic country subreddits, many of them are interestingly enough situated in between "paris" and "france". It also has to be mentioned, that both "france" and "paris" are mainly french speaking. We suppose this will lessen the hyperlinks to and from those subreddits, but this is outside the scope of this project.

<figure id="fig-cluster-graph-charlie-hebdo">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/clusters/temporal_cluster_graph_Charlie_Hebdo.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Daily hyperlink activities around the terrorist attacks on Charlie Hebdo in January 2015.
  </figcaption>
</figure>


We can see that this event does **not** show a significant peak [Figure ???](#fig-before-after-graph-charlie-hebdo) when compared with the periods before and after. This is true for even small periods of time, this means even the momentary impact of the event in this cluster is surprisingly small.


<figure id="fig-before-after-graph-charlie-hebdo">
  <div class="plotly-embed-smaller">
    <iframe
      src="{{ 'assets/img/plots/before_after_during_World_Geography_2015_01_07.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Activities the year before and after the terrorist attacks.
  </figcaption>
</figure>

Looking more exactly at the relationship of the subreddits "france" and "paris", it is possible to firstly deduce a newly (re-) formed but temporary relationship between the two, due to the event on January 7th. This being said, the connections between the two subreddits are sparse and far between, a statistical analysis will quickly find the connection to be significant even if it only lasts a few days or weeks. What we can say with certainty, is that the sentiment of those connections is more positive than most of the rest of the time in that year. This is without a doubt due to expressions of sympathy from one to another.

#### Paris Attacks (2015) — emotion without structural change

<figure id="fig-cluster-graph-bataclan">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/clusters/temporal_cluster_graph_bataclan.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Daily hyperlink activities around the November 2015 terrorist attacks in Paris.
  </figcaption>
</figure>

[Figure ???](#fig-cluster-graph-bataclan) shows similar trends as [Figure ???](#fig-cluster-graph-charlie-hebdo), though the immediate days following the attack on 13 November 2015 show more intensive connections than what happened in the attacks on Charlie Hebdo in the beginning of the same year.

The difference between the two events is even more visible when comparing the before and after of the two terrorist attacks. The attack on November 13 is significantly more important in the whole cluster than the the posts in a year before and after (See [Figure ???](#fig-before-after-graph-bataclan)) The earlier mentioned temporary increase in relationship between "france" and "paris" in the attacks on Charlie Hebdo can be seen in the whole cluster for the attacks in November.


<figure id="fig-before-after-graph-bataclan">
  <div class="plotly-embed-smaller">
    <iframe
      src="{{ 'assets/img/plots/before_after_during_World_Geography_2015_11_13.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Hyperlink activities in the geography cluster a year before and after the november attacks.
  </figcaption>
</figure>




#### Ebola (2014) — fear without diffusion

**I vote to exclude this here**

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

