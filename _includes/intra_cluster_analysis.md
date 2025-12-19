## 5. Zooming into Events and Communities (Template)

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

<details markdown="1">
  <summary>Politics</summary>

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

  In [figure ???](#fig-sliding-event-intensity-politics) the sliding event intensity is shown. For this graph, the absolute number of hyperlinks was averaged inside a timeframe of 3 days to show the the local trends without taking into account the constant rising in post numbers. What really comes apparent are two things: The first is that with increasing number of hyperlinks, the variation in number of posts becomes more erratic. This may be due to a fast reaction of the subreddits on events, but it could also be due to increasing numbers of multiple link targets in one post as more posts with links happen overall. 

  The second thing to note is the intensity of the "post-election" collapse in link numbers. Even when averaging the surrounding days, the intensity falls significantly and permanently. The existence of this depression supports the thesis that the erratic-ness of the post intensity is due to world events, as after the major world event, the erratic-ness decreases as well.

  <figure id="fig-sliding-event-intensity-politics">
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

  #### US Presidential Election (2016) — maximum polarization, minimal rewiring

  As shown in [Figure ???](#fig-cluster-graph-US-election), in the time period around the US election, everything is about Donald Trump or the election. In the figure, the subreddits "the_donald", "conspiracy", "politics" and "hillaryclinton" are highlighted and it can clearly be seen how dominating they, and especially "the_donald" and their close neighbors, are.


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

  The difference of intra-cluster daily post counts before and after November 8th is shown in [figure ???](#fig-before-after-graph-US-election) and it confirms what we saw in the [temporal graph earlier:](#fig-normalized-weekly-politics) The hyperlinks between communities increase significantly around the election and then decrease again in the period after.

  <figure id="fig-before-after-graph-US-election">
    <div class="plotly-embed-smaller">
      <iframe
        src="{{ 'assets/img/plots/before-after-comparison_politics_2016_11_08.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure ???.</strong> Activities the year before and after the US election.
    </figcaption>
  </figure>

  We may even statistically capture this increase in posts. If our hypothesis is that an increase of hyperlink connections between "politcs" and "the_donald" is due to an event with our null hypothesis being that this is not the case, we may do a t-test during the run-up of the election and evaluate it's p-value. On the date of the election, we obtain a p-value of 0.081. While this is not decisive, it strongly indicates a statistical correlation between the event and the increase in hyperlink connections.

  Using the same methodology between the subreddits "the_donald" and "conspiracy", an even stronger evidence is obtained. The p-value is 0.034, a value which lets us completely reject the null hypothesis. For both relations there is a statistically shown low stability of connections. Which, again considering the "post-election" collapse, makes sense. At least for a short moment, people distanced themselves from politics.

  The pause does not last though. The connections forged during the elections are here to stay. The links from "the_donald" with "politics" due to the election fade very slowly with a statistical half life of the connection being 55 weeks. This is very long, for comparison, the half life between "the_donald" and "news" is 22 weeks. In the case of "conspiracy" and "the_donald", the connection does not even decay, but rather increase in the weeks following. A trend well reflected in real life during both of Donald Trump's periods in office.

  #### Crimea Annexation (2014) — geopolitics without cultural spillover

  **I'll look into either this or Brexit more exactly. The other I'll only write short sentence about**

  *Despite global media coverage and rising international tension, the annexation of
  Crimea remains almost entirely confined to news and geopolitics communities.
  Interaction levels with entertainment remain flat, no durable bridges emerge, and
  several ties even weaken.*

  *Geopolitical distance matters. When a political event feels remote — geographically
  or emotionally — it does not penetrate cultural spaces.*

  #### Brexit Referendum (2016) — politics enters daily life, but stops short of culture

  *Brexit represents a clear step forward in spillover. Political discussion expands
  outward into social and everyday communities, reflecting how deeply the referendum
  affected identity, family, and daily conversation.*

  *However, this expansion remains fragile. While interaction intensity rises
  temporarily, no long-term cultural bridges form. Entertainment communities remain
  largely untouched. Politics becomes personal — but not cultural.*



  #### Politics → Entertainment: what we learn

  Across all three political events:

  - Politics sometimes spills into social spaces  
  - Politics rarely spills into entertainment  
  - Politics never durably rewires cultural communities  

  Entertainment remains structurally insulated from political shocks.

</details>

---

### Does culture ever pull politics in?  
**Entertainment → Politics**

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

The daily activity in the cluster predictably increases over time if only due to increased size of reddit itself. The analysis shows some strong peaks, though we were unable to relate them to a specific event. No event is dominating enough for it to be easily visible on the temporal graph and the amount of posts increases near linearly over time.

<figure id="fig-sliding-event-intensity-entertainment">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/plots/sliding_event_intensity_entertainment.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Sliding event intensity in the entertainment cluster.
  </figcaption>
</figure>

Analyzing the sliding event intensity of the entertainment cluster in [figure ???](#fig-sliding-event-intensity-entertainment) with the [sliding event intensity of the politics cluster](fig-sliding-event-intensity-politics) seen earlier, it is possible to make out how the erraticness of the cluster intensity. While the sliding event intensity of the politics cluster changes over time based on an event, the entertainment cluster sliding event intensity has near unchanging peak-to-peak values and frequency. 

Back inside the entertainment cluster when analyzing the top subreddits by hyperlink numbers, we can notice most of them are generalist or humorist subreddits which cover a whole branch of media. The first non-generalist subreddit is "pokemongivaway", though being a giveaway subreddit it is heavily skewed towards linking and being linked to. The second interesting one is "starwars" and as it is, there was a huge blockbuster release in 2015, so inside the period of our dataset.

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

#### Star Wars: *The Force Awakens* (December 2015) — massive attention, zero political pull

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


#### Oscars 2016 (*#OscarsSoWhite*) — culture brushes politics, briefly

**I'll write a short sentence about it later, but we could also delete it this part.**

Unlike *Star Wars*, the Oscars explicitly intersect with political themes: diversity,
representation, and inequality. Here, we observe a short-lived increase in
interaction between entertainment and politics.

But the effect does not stabilize. No new bridges form, correlations return to
baseline, and the network quickly relaxes. Culture can open political conversations —
but it does not reorganize them.

#### Game of Thrones, Season 6 (April - June 2016) — culture rewires itself, not politics

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


### Terrorism vs. health: symbolism matters more than severity

Another title proposition if we exclude Ebola:
"Terror attacks in Paris: Do more deaths equal more attention?"

#### Charlie Hebdo (January 2015) — politics becomes social

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

#### Paris Attacks (November 2015) — emotion without structural change

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

**I vote to exclude this. It covers a too big of a period and is impossible to analyze**

Ebola generates fear, but no political or social spillover. Health discussion
contracts inward, remaining technical and informational. Severity alone is not
enough; symbolism is decisive.



### Sports

#### Some important championship. Maybe football world championship, maybe super bowl, maybe olympic games.



### Gaming

The cluster of gaming is big and, in Reddit terms, rather important. It's main contributors to the hyperlink lists are a mix of game specific subreddits such as "leagueoflegends", "dota" or "smashbros" or general gaming subreddits like "gaming", "gamingcirclejerk" or in a farther sense also "pcmasterrace". 

<figure id="fig-plot-top-subreddits-gaming">
  <div class="plotly-embed-smaller">
    <iframe
      src="{{ 'assets/img/plots/top-subreddit-interaction-gaming.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Top subreddits in the gaming cluster by number of interactions.
  </figcaption>
</figure>

#### Pokemon Go; an initial trend or long lasting connections?

In this analysis, we concentrate ourselves not on an important event inside an existing structure, like we could do for some world championship in League of Legends or CS:GO, but rather the impact of a new game: Pokémon Go.

Pokémon Go, the mobile game which popularized the use of augmented reality technology, was released on most of the world in June 2016. Unsurprisingly, most subreddits relating to it where only started after its release. An important exception is the main subreddit "pokemongo" which was probably created when the game was first still in development. The cluster graph in [figure ???](#fig-cluster-graph-pokemongo) indicates strongly when most of the regional "sub-communities" of the main subreddit were created. Highlighted are communities relating to "pokemon" or "pokemongo".

<figure id="fig-cluster-graph-pokemongo">
  <div class="plotly-embed">
    <iframe
      src="{{ 'assets/img/clusters/temporal_cluster_graph_pokemongo.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Daily hyperlink activities around releases of Pokémon Go around the world.
  </figcaption>
</figure>

In June alone, the main subreddit "pokemongo" formed relations with at least 89 subreddits which were linked to or linked from at least once more in the next two months. Supporting our theory of the game's release being the reason for increased local connections are statistical t tests which admit a p value against the null hypothesis of there being no relation of 0.045 between the subreddits "pokemon" and "pokemongo. This together with a big Cohen's d 0f 0.618, lets us conclude that there, in fact, is a correlation between the release of the game Pokémon Go and the subreddit hyperlinks connecting to the subreddit "pokemongo".

### Other sport?

Would be interesting to see if a big event (such as LoL championships) which is not important for the wider public but important for a big subreddit has a cluster-wide impact. We could theorize, that only big events or events in big subreddits are important for the whole cluster.


### Others? collective attention


**Either 1st of April (r/place) or Christmas or both would be funny.**


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
