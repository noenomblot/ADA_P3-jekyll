# 5. Zooming into Events and Communities 

Well, now that you have seen how communities interact **with one another** on Reddit, you might be wondering what all of this means if you mostly stay within a single space. Many users are lurkers or regular contributors to just one community, with little interest in crossing categories.

That intuition is fair and the data supports it. The majority of hyperlink interactions on Reddit happen **within the same community**. So even if you never leave your favorite subreddit, shifts in hyperlink traffic still shape what you see, what gains visibility, and how discussion evolves.


<figure class="flourish-figure">
  <div class="flourish-embed flourish-chord" data-src="visualisation/26916041">
    <script src="https://public.flourish.studio/resources/embed.js">
    </script>
    <noscript>
      <img src="https://public.flourish.studio/visualisation/26916041/thumbnail" width="100%" alt="chord visualization" />
    </noscript>
  </div>

  <figcaption>
    <strong>Figure 14.</strong> Chord diagram of interactions within and between Reddit communities.
  </figcaption>
</figure>

To understand how major events affect users at this more personal scale, the analysis now zooms inward. Instead of looking at connections *between* clusters, we focus on **intra-cluster dynamics** : how a single community reacts to shocks, and how large global events compare to smaller, more localized moments.

---

### Inside Communities: Three Case Studies

Below, we explore three different kinds of events inside their main clusters:

- a **major political shock** (the 2016 U.S. election) inside the Politics/News cluster,  
- a **viral game release** (*Pokémon GO*) inside the Gaming cluster,  
- and **two terrorist attacks** of different magnitude within the World/Geography cluster.

Each case is folded into a collapsible block so you can open only the stories you care about.

---

<details class="event-block">
  <summary>
    <span class="event-pill">Politics cluster</span>
    <span>Election Shocks and Their Aftermath</span>
  </summary>
  <div markdown="1">

### Inside a Community: A Case Study of Politics

What happens within a cluster when a major event unfolds? To answer this, we focus on the politics/news cluster.

Unsurprisingly, the most central subreddits in terms of internal hyperlink activity are explicitly political. At the core sits **r/The_Donald**, a right-wing subreddit (now banned) that played a dominant role during the 2016 U.S. presidential election. Closely following are **r/conspiracy**, **r/politics**, and **r/news** , heavily involved in the same election cycle, but often positioned in opposition to *The_Donald*. In this sense, *r/politics* and *r/news* act as a counter-pole within the cluster, anchoring a different political narrative.

<figure id="fig-plot-top-subreddits-politics">
  <div class="plotly-embed-top">
    <iframe
      src="{{ 'assets/img/plots/top-subreddit-interaction-politics.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure 15.</strong> Top subreddits in the politics/news cluster.
  </figcaption>
</figure>

This internal tension makes the politics cluster an ideal lens through which to study how events reshape attention.

#### Reading the Pulse of Political Attention

Figure&nbsp;[16](#fig-sliding-event-intensity-politics) shows the **sliding event intensity** within the politics cluster. To isolate short-term reactions, the absolute number of hyperlinks is averaged over a three-day window. This smoothing removes long-term growth in Reddit activity and lets local fluctuations come into focus.

Two patterns immediately stand out.

<figure id="fig-sliding-event-intensity-politics">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/plots/sliding_event_intensity_politics.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure 16.</strong> Sliding event intensity in the politics/news cluster.
  </figcaption>
</figure>

First, as hyperlink activity increases, posting behavior becomes noticeably more erratic. Peaks grow sharper and fluctuations more volatile, reflecting rapid, real-time reactions to unfolding events. Major moments do not just add posts. They create denser, more unstable bursts of interaction.

Second and far more striking is the **post-election collapse**. Even after averaging across neighboring days, hyperlink intensity drops sharply following the 2016 election and does not recover over the remaining observation window. The fall is not a brief dip, but a sustained depression in activity.

This collapse provides strong evidence that the heightened volatility observed earlier is driven by real-world events rather than organic growth alone. Once the defining political moment passes, the network settles: activity stabilizes, fluctuations shrink, and the intense, reactive behavior fades.

In other words, major world events do not just create spikes. They temporarily change the **internal rhythm** of communities. Within politics, the election acts as a gravitational center, pulling attention inward and amplifying interaction. Once that center disappears, so does the chaos it generated. Even for users who never leave a single subreddit, the world still arrives, quietly restructuring the conversations around them.

#### Who Dominated the Cluster During the Election?

We now zoom further into **how the U.S. presidential election reorganized the internal structure of the politics cluster itself**. Rather than looking at aggregate intensity alone, this view exposes *who* dominated attention and *how long* those effects endured.

As shown in Figure&nbsp;[17](#fig-cluster-graph-US-election), the period surrounding the U.S. election is overwhelmingly centered on Donald Trump and the election itself. A small set of subreddits, **r/The_Donald**, **r/conspiracy**, **r/politics**, and **r/hillaryclinton**, rise above the rest, reshaping the internal topology of the cluster.

<figure id="fig-cluster-graph-US-election">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/clusters/temporal_cluster_graph_US_election.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure 17.</strong> Daily hyperlink activities around the U.S. election.
  </figcaption>
</figure>

Among them, **r/The_Donald** is unmistakably dominant. Its position at the center of the graph, surrounded by a dense neighborhood of closely connected subreddits, reveals how attention gravitated toward a single ideological hub. The cluster does not simply grow more active; it becomes structurally skewed, with influence concentrating around a few key actors.

This structural dominance is mirrored in posting behavior. The difference in intra-cluster daily post counts before and after November&nbsp;8 is shown in Figure&nbsp;[18](#fig-before-after-graph-US-election).

<figure id="fig-before-after-graph-US-election">
  <div class="plotly-embed-smallest">
    <iframe
      src="{{ 'assets/img/plots/before-after-comparison_politics_2016_11_08.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure 18.</strong> Activities the year before and after the U.S. election.
  </figcaption>
</figure>

In the run-up to the election, hyperlink activity between political communities rises sharply, reflecting heightened engagement and cross-referencing. Immediately after the election, however, this intensity drops: the network exhales. While activity does not vanish, the extraordinary level of interconnection fades, marking the end of the election-driven surge.

#### How Long Do Election-Induced Links Last?

These visual patterns can also be detected statistically. If the hypothesis is that the election itself drove the increase in hyperlink connections, particularly between **r/politics** and **r/The_Donald**, this can be tested directly. Using a t-test over the pre-election period, the p-value on election day reaches **0.081**. While not fully decisive, this strongly suggests a correlation between the event and the observed rise in hyperlink activity.

The signal becomes clearer when examining the relationship between **r/The_Donald** and **r/conspiracy**. Applying the same methodology yields a p-value of **0.034**, allowing the null hypothesis to be rejected. In both cases, the connections formed around the election show **low stability**, consistent with the sharp post-election decline in activity: for a brief moment, attention pulls away from politics altogether.

Yet the pause is temporary. The links forged during the election do not simply disappear. They decay slowly, and in some cases, not at all. The connection between **r/The_Donald** and **r/politics** exhibits a statistical half-life of **55 weeks**, an exceptionally long persistence. For comparison, the half-life of the connection between **r/The_Donald** and **r/news** is only **22 weeks**.

Even more striking, the relationship between **r/conspiracy** and **r/The_Donald** does not decay in the weeks following the election. Instead, it continues to strengthen, a pattern that closely mirrors real-world political dynamics during Donald Trump’s time in office.

Taken together, these results show that major political events do more than generate temporary noise. They **restructure communities internally**, elevate specific actors, and forge connections that can persist long after the headlines fade. Even when activity subsides, the network remembers.

  </div>
</details>

---

<details class="event-block">
  <summary>
    <span class="event-pill">Gaming cluster</span>
    <span>*Pokémon GO*: A Localized Shock</span>
  </summary>
  <div markdown="1">

### Do Smaller Events Evoke a Similar Reaction? Release of *Pokémon GO*

In the case of the U.S. election, we saw one of the most important events on Reddit, culminating in an enormous, cluster-wide reaction. A natural follow-up question is: **how does Reddit react to something more niche?**

For this, we examine the release of the augmented-reality mobile game *Pokémon GO*. The subreddits most central to this event are **r/pokemon** and **r/pokemongo**, both belonging to the Gaming cluster. With 621 hyperlink interactions over the observation period, **r/pokemongo** ranks as the 32nd most connected subreddit within the cluster, which is impressive for a community that only became active after the game’s release in June 2016.

<figure id="fig-plot-top-subreddits-gaming">
  <div class="plotly-embed-top">
    <iframe
      src="{{ 'assets/img/plots/top-subreddit-interaction-gaming.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure 19.</strong> Top subreddits in the gaming cluster by number of interactions.
  </figcaption>
</figure>

A major reason a subreddit created in 2016 can still be in the top 50 is the **unusual structure** of the *Pokémon GO* community. Instead of remaining centralized in a single global subreddit, regional groups appeared almost immediately. For a game that (before COVID-19) rewarded walking outside and meeting other players, local coordination made perfect sense.

In Figure&nbsp;[20](#fig-cluster-graph-pokemongo), the daily evolution of activity surrounding the worldwide release in June can be clearly traced. Highlighted in the analysis are the primary subreddit **r/pokemongo**, the broader franchise hub **r/pokemon**, and several regional offshoots, capturing both global and localized engagement patterns.

<figure id="fig-cluster-graph-pokemongo">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/clusters/temporal_cluster_graph_pokemongo.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure 20.</strong> Daily hyperlink activities around releases of *Pokémon GO* around the world.
  </figcaption>
</figure>

#### Local Shock, Measurable but Limited

In June alone, **r/pokemongo** established connections with at least **89 other subreddits** that continued to exchange hyperlinks at least once over the following two months. This rapid expansion reflects a burst of attention directly tied to the game’s worldwide release.

Statistical tests support this interpretation. Testing the null hypothesis that the increase in hyperlinks between **r/pokemon** and **r/pokemongo** is unrelated to the release yields a **p-value of 0.045** and a **Cohen’s d of 0.618**, indicating a moderately strong effect. The launch of *Pokémon GO* is therefore strongly associated with the surge in hyperlink activity directed toward **r/pokemongo**.

The natural follow-up question is whether this intense burst of activity mattered for the Gaming cluster as a whole. Here, the answer is more restrained.

Neither **r/pokemon** nor **r/pokemongo** ranks among the top ten subreddits by total hyperlink interactions within the cluster (see Figure&nbsp;[19](#fig-plot-top-subreddits-gaming)). Highly dominant communities such as **r/leagueoflegends** exert far greater gravitational pull, effectively dampening the cluster-wide impact of even globally popular releases.

In this sense, *Pokémon GO* represents a **localized shock** : powerful within its immediate neighborhood, yet unable to overcome the structural inertia imposed by entrenched hubs. Together with the political case study, this contrast highlights a key insight: **not all viral moments scale equally**. Some events reorganize entire clusters, while others burn brightly within a confined region of the network before settling back into the existing hierarchy.

  </div>
</details>

---

<details class="event-block">
  <summary>
    <span class="event-pill">World cluster</span>
    <span>Two Terrorist Attacks in France: Unequal Reactions</span>
  </summary>
  <div markdown="1">

### What Importance Must an Event Have for Reddit to React? — Terrorism

After studying the reaction of the politics cluster to a large-scale event (the U.S. elections) and a medium-scale one (*Pokémon GO*), we turn to the **World/Geography cluster** to explore the boundary of event impact. Here, we compare two terrorist attacks in Paris in 2015:

- the **Charlie Hebdo** shooting on January 7,  
- and the coordinated attacks of **November 13** (often associated with the Bataclan).  

Their geographical and temporal closeness makes them an ideal pair for analyzing how a cluster reacts to events of different magnitude.

From the start of January, we observe the immediate reaction of the Geography/World cluster in Figure&nbsp;[21](#fig-cluster-graph-charlie-hebdo). Days after the Charlie Hebdo attack, there are some connections from and to the highlighted subreddits **r/france** and **r/paris**, but the increase is modest compared to earlier examples.

<figure id="fig-cluster-graph-charlie-hebdo">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/clusters/temporal_cluster_graph_Charlie_Hebdo.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure 21.</strong> Daily hyperlink activities around the terrorist attacks on Charlie Hebdo in January 2015.
  </figcaption>
</figure>

The observations from the temporal clustering graph are confirmed in Figure&nbsp;[22](#fig-before-after-graph-charlie-hebdo). The average number of hyperlink connections in the year before, the year after, and the days around the incident reveals **no significant increase** in connections within the Geography/World cluster.

<figure id="fig-before-after-graph-charlie-hebdo">
  <div class="plotly-embed-smallest">
    <iframe
      src="{{ 'assets/img/plots/before_after_during_World_Geography_2015_01_07.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure 22.</strong> Hyperlink activities the year before and after the Charlie Hebdo attack.
  </figcaption>
</figure>

Looking more closely at the relationship between **r/france** and **r/paris**, we can detect a newly formed but temporary relationship likely triggered by the event on January 7. The connections remain sparse, but those that do appear predominantly convey positive and supportive sentiment.

By contrast, Reddit’s reaction to the November 13 attacks is much stronger.

<figure id="fig-cluster-graph-bataclan">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/clusters/temporal_cluster_graph_bataclan.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure 23.</strong> Daily hyperlink activities around the November 2015 terrorist attacks in Paris.
  </figcaption>
</figure>

The group around **r/france** shows a clear surge in hyperlink connections, although it is difficult to attribute the entire increase solely to the attacks. The difference between the two events becomes even more visible when looking at the average interaction graph before and after November&nbsp;13 in Figure&nbsp;[24](#fig-before-after-graph-bataclan).

<figure id="fig-before-after-graph-bataclan">
  <div class="plotly-embed-smallest">
    <iframe
      src="{{ 'assets/img/plots/before_after_during_World_Geography_2015_11_13.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure 24.</strong> Hyperlink activities in the Geography/World cluster the year before and after the November attacks.
  </figcaption>
</figure>

Here, a **cluster-wide increase** in hyperlink connections appears around the date of the attacks, followed by a gradual return to baseline. Locally, connections between **r/france** and **r/paris** strengthen again, but only temporarily.

While these events are first and foremost human tragedies, this analysis shows that the magnitude of an incident matters for how strongly Reddit reacts. Reddit’s engagement should not be interpreted as a measure of real-world loss, but the patterns suggest, contrary to earlier findings, that after a large-scale catastrophe, inter-community engagement is often driven by expressions of empathy that are intense but short-lived, rather than by lasting structural change.

  </div>
</details>

---

## Takeaways from Intra-Cluster Analysis

Bringing together the intra-cluster analyses above, several clear patterns emerge that help explain how Reddit communities respond when the outside world intrudes.

### What We Learn from Inside the Clusters

1. **Big events trigger big reactions.**  
   The more universally important an event is, the stronger and more sustained the response within a cluster. The 2016 U.S. presidential election illustrates this vividly, with activity steadily intensifying in the lead-up to election day, followed by a pronounced and lasting drop in hyperlink activity once the event passed.

2. **Local importance does not guarantee global impact.**  
   Some events resonate powerfully within a narrow region of the network without reshaping the cluster as a whole. The release of *Pokémon GO* generated a clear surge of activity around **r/pokemongo**, yet this excitement remained largely localized and failed to propagate across the broader Gaming cluster.

3. **Event magnitude shapes whether clusters react at all.**  
   Not all events cross the threshold required to mobilize an entire cluster. Smaller shocks, like the Charlie Hebdo attack, leave only faint structural traces, while larger ones, such as the November 2015 attacks, trigger visible but temporary reorganizations. The likelihood of a collective reaction increases with the perceived impact of the event, suggesting an implicit tipping point beyond which attention spreads from local neighborhoods to the cluster at large.
