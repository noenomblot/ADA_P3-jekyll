## 5. Zooming into Events and Communities 



Well now that you have seen how communities interact **with one another** on Reddit, you might be wondering what all of this means if you mostly stay within a single space. Many users are lurkers or regular contributors to just one community, with little interest in crossing categories.

That intuition is fair and the data supports it. The majority of hyperlink interactions on Reddit happen **within the same community**. So even if you never leave your favorite subreddit, shifts in hyperlink traffic still shape what you see, what gains visibility, and how discussion evolves.

<div class="flourish-embed flourish-chord" data-src="visualisation/26916041">
  <script src="https://public.flourish.studio/resources/embed.js">
  </script>
  <noscript>
    <img src="https://public.flourish.studio/visualisation/26916041/thumbnail" width="100%" alt="chord visualization" />
  </noscript>
</div>

To understand how major events affect users at this more personal scale, the analysis now zooms inward. Instead of looking at connections *between* clusters, we focus on **intra-cluster dynamics** — how a single community reacts to shocks, and how large global events compare to smaller, more localized moments.

---

## Inside a Community: A Case Study of Politics

<<<<<<< HEAD
What happens *within* a cluster when a major event unfolds? To answer this, we focus on the politics/news cluster.

Unsurprisingly, the most central subreddits in terms of internal hyperlink activity are explicitly political. At the core sits **r/The_Donald**, a right-wing subreddit (now banned) that played a dominant role during the 2016 U.S. presidential election. Closely following are **r/conspiracy**, and then **r/politics** and **r/news** — both heavily involved in the same election cycle, but generally positioned in opposition to *The_Donald*. In this sense, *r/politics* and *r/news* act as a counter-pole within the cluster, anchoring a different political narrative.
=======
### If a big event happens, how do clusters react? - US Presidential Election 2016

  In the politics/news cluster, the biggest subreddits in terms of subreddit interactions are unsurprisingly political. The biggest being "the_donald" a right wing, now banned, subreddit supporting Donald Trump especially during the 2016 US presidential election. The second biggest is "conspiracy" and the third and fourth "politics" and "news", two subreddits also strongly involved in the US election cycle of 2016. It has to be noted that "politics" and "news" tend to be anti-Trump and are taken as "the_donald"s counter-pole in our analysis.
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546

<figure id="fig-plot-top-subreddits-politics">
    <div class="plotly-embed-top">
      <iframe
        src="{{ 'assets/img/plots/top-subreddit-interaction-politics.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure ???.</strong> Top subreddits in the politics/news cluster.
    </figcaption>
  </figure>

This internal tension makes the politics cluster an ideal lens through which to study how events reshape attention.


### Reading the Pulse of Political Attention

Figure [???](#fig-sliding-event-intensity-politics) shows the **sliding event intensity** within the politics cluster. To isolate short-term reactions, the absolute number of hyperlinks is averaged over a three-day window. This smoothing removes the long-term growth in Reddit activity and allows local fluctuations to come into focus.



Two patterns immediately stand out.

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

<<<<<<< HEAD
First, as hyperlink activity increases, posting behavior becomes noticeably more erratic. Peaks grow sharper, and fluctuations more volatile. This likely reflects rapid, real-time reactions to unfolding events. At the same time, it may also be amplified by structural effects — as major moments trigger more posts containing multiple hyperlinks, the system becomes denser and more unstable in the short term.

Second — and far more striking — is the **post-election collapse**. Even after averaging across neighboring days, hyperlink intensity drops sharply following the 2016 election and does not recover. The fall is not a brief dip, but a sustained depression in activity.
=======
  As shown in [Figure ???](#fig-cluster-graph-US-election), in the time period around the US election, everything is about Donald Trump or the election. In the figure, the subreddits "the_donald", "conspiracy", "politics" and "hillaryclinton" are highlighted and it can clearly be seen how dominating they, and especially "the_donald" and their close neighbors, are.
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546

This collapse provides strong evidence that the heightened volatility observed earlier is driven by real-world events rather than organic growth alone. Once the defining political moment passes, the network settles. Activity stabilizes, fluctuations shrink, and the intense, reactive behavior fades.


In other words, major world events do not just create spikes — they reshape the internal rhythm of communities. Within politics, the election acted as a gravitational center, pulling attention inward and amplifying interaction. Once that center disappeared, so did the chaos it generated.

Even for users who never leave a single subreddit, the world still arrives — quietly restructuring the conversations around them.

We now zoom further into **how the U.S. presidential election reorganized the internal structure of the politics cluster itself**. Rather than looking at aggregate intensity alone, this view exposes *who* dominated attention and *how long* those effects endured.



As shown in [Figure ???](#fig-cluster-graph-US-election), the period surrounding the U.S. election is overwhelmingly centered on Donald Trump and the election itself. A small set of subreddits — **r/The_Donald**, **r/conspiracy**, **r/politics**, and **r/hillaryclinton** — rise above the rest, reshaping the internal topology of the cluster.

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

Among them, **r/The_Donald** is unmistakably dominant. Its position at the center of the graph, surrounded by a dense neighborhood of closely connected subreddits, reveals how attention gravitated toward a single ideological hub. The cluster does not simply grow more active; it becomes structurally skewed, with influence concentrating around a few key actors.

This structural dominance is mirrored in posting behavior. The difference in intra-cluster daily post counts before and after November 8 is shown in [Figure ???](#fig-before-after-graph-US-election).

 <figure id="fig-before-after-graph-US-election">
    <div class="plotly-embed-smallest">
      <iframe
        src="{{ 'assets/img/plots/before-after-comparison_politics_2016_11_08.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure ???.</strong> Activities the year before and after the US election.
    </figcaption>
  </figure>

In the run-up to the election, hyperlink activity between political communities rises sharply, reflecting heightened engagement and cross-referencing. Immediately after the election, however, this intensity drops. The network exhales. While activity does not vanish, the extraordinary level of interconnection fades, marking the end of the election-driven surge.


<<<<<<< HEAD

These visual patterns can also be detected statistically. If the hypothesis is that the election itself drove the increase in hyperlink connections — particularly between **r/politics** and **r/The_Donald** — this can be tested directly. Using a t-test over the pre-election period, the p-value on election day reaches **0.081**. While not fully decisive, this result strongly suggests a correlation between the event and the observed rise in hyperlink activity.

The signal becomes even clearer when examining the relationship between **r/The_Donald** and **r/conspiracy**. Applying the same methodology yields a p-value of **0.034**, allowing the null hypothesis to be confidently rejected. In both cases, the connections formed around the election show **low stability**, consistent with the sharp post-election decline in activity. For a brief moment, attention pulls away from politics altogether.

Yet the pause is temporary.

The links forged during the election do not simply disappear — they decay slowly, and in some cases, not at all. The connection between **r/The_Donald** and **r/politics** exhibits a statistical half-life of **55 weeks**, an exceptionally long persistence. For comparison, the half-life of the connection between **r/The_Donald** and **r/news** is only **22 weeks**.

Even more striking, the relationship between **r/conspiracy** and **r/The_Donald** does not decay in the weeks following the election. Instead, it continues to strengthen — a pattern that closely mirrors real-world political dynamics during both of Donald Trump’s terms in office.

Taken together, these results show that major political events do more than generate temporary noise. They **restructure communities internally**, elevate specific actors, and forge connections that can persist long after the headlines fade. Even when activity subsides, the network remembers.

=======
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546
---

### Do smaller events evoke a similar reaction? - Release of *Pokémon Go*

<<<<<<< HEAD
  In the case of the US election, we saw an important, if not the most important, event on Reddit which culminates in an enormous, cluster wide reaction. Now it is only pertinent to ask, how Reddit's reaction to something more niche would be. For this, we will look at the release of the augmented reality mobile game *Pokémon Go*. The subreddits most central to this event are **r/pokemon** and **r/pokemongo**, both belonging to the Gaming cluster. With 621 hyperlink interactions over the available observation period, r/pokemongo ranks as the 32nd most connected subreddit within the cluster. This level of importance is particularly notable given that the subreddit only became active after the game’s release in June 2016, meaning it accumulated this influence within just the second half of the data collection window.
=======
  In the case of the US election, we saw an important, if not the most important, event on Reddit which culminates in an enormous, cluster wide reaction. Now it is only pertinent to ask, how Reddit's reaction to something more niche would be. For this, we will look at the release of the augmented reality mobile game *Pokémon Go*. The subreddits important for this event are called "pokemon" and "pokemongo", both situated in the Gaming cluster. With 621 hyperlink interactions during the period of the available dataset and thus the 32nd most important subreddit within the cluster, the subreddit "pokemongo" could still be counted as one of the more important ones. This is especially considering the subreddit becoming active only after the game's release in June 2016, i.e. in only the second half of the data acquisition period.
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546


  <figure id="fig-plot-top-subreddits-gaming">
    <div class="plotly-embed-top">
      <iframe
        src="{{ 'assets/img/plots/top-subreddit-interaction-gaming.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure ???.</strong> Top subreddits in the gaming cluster by number of interactions.
    </figcaption>
  </figure>


<<<<<<< HEAD
  A big reason for why a subreddit created in 2016 can still be in the top 50, is the more or less unique development the pokemongo community followed: Instead of only being organized in a global subreddit, almost immediately regional groups were formed. This makes sense for a game which, [before Covid](https://www.gamedeveloper.com/design/how-i-pokemon-go-i-evolved-in-response-to-the-covid-19-pandemic){:target="_blank"}, was a local game with multiplayer aspects. In figure [figure ???](#fig-cluster-graph-pokemongo) the daily evolution of activity surrounding the worldwide release in June can be clearly traced. Highlighted in the analysis are the primary subreddit r/pokemongo, the broader franchise hub r/pokemon, and several regional offshoots associated with each, capturing both global and localized engagement patterns.
=======
  A big reason for why a subreddit created in 2016 can still be in the top 50, is the more or less unique development the pokemongo community followed: Instead of only being organized in a global subreddit, almost immediately regional groups were formed. This makes sense for a game which, [before Covid](https://www.gamedeveloper.com/design/how-i-pokemon-go-i-evolved-in-response-to-the-covid-19-pandemic){:target="_blank"}, was a decentralized/local game with multiplayer aspects. In figure [figure ???](#fig-cluster-graph-pokemongo) the daily development around the worldwide releases in June can be followed. Highlighted are the main subreddit "pokemongo", the subreddit "pokemon" and various regional offshoot relating to either of them.
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546

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

<<<<<<< HEAD
 Building on the earlier observations, we now turn to how the release of *Pokémon GO* reshaped interactions **within** the Gaming cluster, and whether these local effects scaled up to influence the cluster as a whole.

In June alone, the main subreddit **r/pokemongo** established connections with at least **89 other subreddits** that continued to exchange hyperlinks at least once over the following two months. This rapid expansion signals more than background noise — it reflects a burst of attention directly tied to the game’s worldwide release.

This interpretation is reinforced statistically. Testing the null hypothesis that the increase in hyperlinks between **r/pokemon** and **r/pokemongo** is unrelated to the release yields a **p-value of 0.045**, allowing the null hypothesis to be rejected at conventional significance levels. Combined with a **Cohen’s d of 0.618**, indicating a moderately strong effect size, the results support a clear conclusion: the launch of *Pokémon GO* is strongly associated with the surge in hyperlink activity directed toward **r/pokemongo**.



The natural follow-up question is whether this locally intense burst of activity mattered for the Gaming cluster as a whole. Here, the answer is more restrained.

Neither **r/pokemon** nor **r/pokemongo** ranks among the top ten subreddits by total hyperlink interactions within the cluster (see [Figure ???](#fig-plot-top-subreddits-gaming)). As a result, their sudden rise, while highly visible at the local level, is insufficient to shift the global structure of the Gaming cluster.

Highly dominant communities such as **r/leagueoflegends** exert far greater gravitational pull, effectively dampening the cluster-wide impact of even globally popular releases. In this sense, *Pokémon GO* represents a **localized shock** — powerful within its immediate neighborhood, yet unable to overcome the structural inertia imposed by entrenched hubs.


Together with the political case study, this contrast highlights a key insight: **not all viral moments scale equally**. Some events reorganize entire clusters, while others burn brightly within a confined region of the network before settling back into the existing hierarchy.

------




### What importance does an event have to have for Reddit to react? - Terrorism

After having studied the reaction of the politics cluster on a large scale event, the US elections, and on an event of medium importance, the release of *Pokémon Go*, we want to test out the boundary of event impact in a case study on two incidences with similar circumstances. Those two incidents under study are the two major terrorist attacks in Paris in 2015. The first incident is the shooting in the Parisian satire magazine *Charlie Hebdo* on January 7, 2015. The second terrorist attack happening in the same year on November 13 in multiple locations throughout the city. Due to their geographical and temporal closeness, they provide an ideal basis to study a subreddit cluster's reaction.

From the start of January, we can see the immediate temporal reaction of the Geography/World cluster in [figure ???](#fig-cluster-graph-charlie-hebdo). Days after the attack, there are some connections from and to the highlighted subreddits "france" and "paris", but the increase is only small compared to earlier examples.
=======
  In June alone, the main subreddit "pokemongo" formed relations with at least 89 subreddits which were linked to or linked from at least once more in the next two months. Supporting our theory of the game's release being the reason for increased hyperlink connections are statistical t-tests which admit a p-value considering the null hypothesis of there being no relation. The p-value testing this theory between the subreddits "pokemon" and "pokemongo" is found to be 0.045. This together with a big Cohen's d 0f 0.618, lets us conclude that there, in fact, is a correlation between the release of the game Pokémon Go and the subreddit hyperlinks connecting to the subreddit "pokemongo". 
  
  Now the logical next question is if the locally relevant increase in hyperlink connections are important for the cluster as a whole. But considering neither "pokemon" nor "pokemongo" being under the top ten subreddits from hyperlink interactions (see [figure ???](#fig-plot-top-subreddits-gaming)), it is unsurprising that we are unable to see a noticeable impact on the cluster as a whole. Subreddits like "leagueoflegends" are just too dominant.

  <figure id="fig-before-after-graph-pokemon_go">
      <div class="plotly-embed-smallest">
        <iframe
          src="{{ 'assets/img/plots/before-after-comparison_gaming_2016_06_11.html' | relative_url }}"
          loading="lazy">
        </iframe>
      </div>
      <figcaption>
        <strong>Figure ???.</strong> Activities the year before and after the release of Pokémon Go.
      </figcaption>
    </figure>

------




### What importance does an event have to have for Reddit to react? - Terrorism

After having studied the reaction of the politics cluster on a huge event, the release of *Pokémon Go*, an event of medium importance, we want to test out the boundary of event impact in a case study on two incidences with similar circumstances. Those two incidents under study are the two major terrorist attacks in Paris in 2015. The first incident is the [shooting in the Parisian satire magazine *Charlie Hebdo*](https://en.wikipedia.org/wiki/Charlie_Hebdo_shooting){:target="_blank"} on January 7, 2015. The second terrorist attack happened in the same year on [November 13 in multiple locations](https://en.wikipedia.org/wiki/November_2015_Paris_attacks){:target="_blank"} throughout the city. Due to their geographical and temporal closeness, they provide an ideal basis to study a subreddit cluster's reaction.

Beginning with the first attack in January, we can see the immediate temporal reaction of the Geography/World cluster in [figure ???](#fig-cluster-graph-charlie-hebdo). The days after the attack, there are some connections from and to the highlighted subreddits "france" and "paris", but the increase is only small compared to earlier examples.
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546

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

<<<<<<< HEAD
The observations from the temporal clustering graph are also be shown in [figure ???](#fig-before-after-graph-charlie-hebdo). The average number of hyperlink connections in the year before, the year after and the days around the incident reveals there is no significant increase of hyperlink connections visible in the Geography/World cluster.
=======
The observations from the temporal clustering graph can also be shown in [figure ???](#fig-before-after-graph-charlie-hebdo), which shows the average number of hyperlink connections in the year before, the year after and the days around the incident. There is no significant increase of hyperlink connections visible in the Geography/World cluster.
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546


<figure id="fig-before-after-graph-charlie-hebdo">
  <div class="plotly-embed-smallest">
    <iframe
      src="{{ 'assets/img/plots/before_after_during_World_Geography_2015_01_07.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Activities the year before and after the terrorist attacks.
  </figcaption>
</figure>

<<<<<<< HEAD
Looking more carefully at the relationship of the subreddits "france" and "paris", we may deduce a newly reformed but temporary relationship between the two, due to the event on January 7th. This being said, the connections between the two subreddits are sparse and far between, but those which do occur predominantly convey positive and supportive sentiments.
=======
Looking more carefully at the relationship of the subreddits "france" and "paris", we may deduce a newly (re-) formed but temporary relationship between the two, due to the event on January 7th. This being said, the connections between the two subreddits are sparse and far between, but those which do occur predominantly convey positive and supportive sentiments.
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546

Reddit's reaction to the second terrorist attack in Paris in 2015 is shown in [figure ???](#fig-cluster-graph-bataclan). Immediately, one can see how this time Reddit reacts much more strongly. The group around "france" especially shows a big increase in hyperlink connections, although it remains unclear to what extent this increase can be directly attributed to the event itself.

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


The difference between the two events is even more visible when looking at the average interaction graph of the subreddit before and after the second attack. Around November 13, there is indeed a cluster wide increase in hyperlink connections which diminishes again in the time after. The same happens locally, the connections between "france" and "paris" increase again but only to then diminish in the time after.


<figure id="fig-before-after-graph-bataclan">
  <div class="plotly-embed-smallest">
    <iframe
      src="{{ 'assets/img/plots/before_after_during_World_Geography_2015_11_13.html' | relative_url }}"
      loading="lazy">
    </iframe>
  </div>
  <figcaption>
    <strong>Figure ???.</strong> Hyperlink activities in the geography cluster a year before and after the november attacks.
  </figcaption>
</figure>

<<<<<<< HEAD
While these events are first and foremost human tragedies, this analysis shows how the magnitude of an incident is important in how big Reddit's reaction becomes. This being said, both attacks are tragedies and Reddit's reaction should not, and does not, quantify the real loss of life in any way. If anything, these patterns suggest that in moments of large-scale human catastrophe, inter-community engagement on Reddit is more often driven by expressions of empathy than by sustained structural change.
=======
While these events are first and foremost human tragedies, this analysis shows how the magnitude of an incident is important in how big Reddit's reaction becomes. Though this being said, both attacks are tragedies and Reddit's reaction should not, and does not, quantify the real loss of life in any way. If anything, these patterns suggest that in moments of large-scale human catastrophe, inter-community engagement on Reddit is more often driven by expressions of empathy than by sustained structural change.
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546

--------------





<!---------
### Entertainment  
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

  The daily activity in the cluster predictably increases over time if only due to increased size of Reddit itself. The analysis shows some strong peaks, though we were unable to relate them to a specific event. No event is dominating enough for it to be easily visible on the temporal graph and the amount of posts increases near linearly over time.

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

  Analyzing the sliding event intensity of the entertainment cluster in [figure ???](#fig-sliding-event-intensity-entertainment) with the [sliding event intensity of the politics cluster](#fig-sliding-event-intensity-politics) seen earlier, it is possible to make out how the erraticness of the cluster intensity. While the sliding event intensity of the politics cluster changes over time based on an event, the entertainment cluster sliding event intensity has near unchanging peak-to-peak values and frequency. 

  Back inside the entertainment cluster when analyzing the top subreddits by hyperlink numbers, we can notice most of them are generalist or humorist subreddits which cover a whole branch of media. The first non-generalist subreddit is "pokemongivaway", though being a giveaway subreddit it is heavily skewed towards linking and being linked to. The second interesting one is "starwars" and as it is, there was a huge blockbuster release in 2015, so inside the period of our dataset.

  <figure id="fig-plot-top-subreddits-entertainment">
    <div class="plotly-embed-top">
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
--------->

<<<<<<< HEAD
<!-- ### Can Longer Lasting Events be Distinguished? - Release of Season 6 of *Game of Thrones*
=======
### Can Longer Lasting Events be Distinguished? - Release of Season 6 of *Game of Thrones*
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546

We come to a topic, which at the time was highly celebrated, but now in hindsight many consider the [beginning of the downfall](https://www.reddit.com/r/gameofthrones/comments/xa3t7d/why_do_people_now_include_season_6_along_7_8_as/) of the popular TV-Series *Game of Thrones*. It, like the election cycle for the US Presidential election, is a longer lasting process due to the nature of the serial release. Usually episodes do not air at the same time, but are published in a weekly frequency. As such, we would not necessarily expect an event, even of the cultural impact of *Game of Thrones* to be well visible on a temporal graph. 

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

Taking into account the normalized weekly intra-cluster activity in [figure ???](fig-plot-normalized-weekly-entertainment) we have to consider the evidence inconclusive. There may be a temporary increase in activity, but due to the erratic nature of the activity in the entertainment cluster, the temporal graph alone does not suffice.

Analyzing the sliding event intensity of the entertainment cluster in [figure ???](#fig-sliding-event-intensity-entertainment), we may again see a slight indication of a continued event between April and July 2016, the smoothed event intensity seems to loose some of it's erraticness and even peaks during this period. But again, we have inconclusive visual evidence of the release of the new *Game of Thrones* season being the reason. 

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


Looking at the clustering graph around the season release in [figure ???](#fig-cluster-graph-gameofthrones), we may see markedly more hyperlink connections after the 24th of April, the date of the episode release. The persisting hyperlink frequency after that date is likely due to the continuous serial nature of the event. Though again, from visual analysis alone, it is impossible to conclude anything concrete.

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

To get evidence for or against the theory of the series releas being the reason for an increased cluster activity, we look at the subreddit relation between the two most important *Game of Thrones* themed subreddits: "freefolk" and "gameofthrones". Statistical evidence shows a slight increase in lasting subreddit relations in the weeks after the release of the first episode. The Cohen's d-test results in a value of 0.484, which signifies a moderate increase in activity and confirms our visual observations of earlier. This being said, the p-value of the event really causing this increase is only 0.16. This is clearly not inside the tolerance of 0.05 usually necessary to exclude the null hypothesis of the increase being not caused by the event. Still, a p-value of this magnitude *may* be an indicator of a correlation.

Now the logical follow up question would be to see the values after the release of the last of season 6's episodes on June 26th.Indeed, we a decay in activity between the two subreddits "freefolk" and "gameofthrones". This decay however is quite a bit smaller, for Cohen's d being -0.374 and here we can reject the hypothesis of the last episode of the season causing a break of previously forged bonds between "freefolk" and "gameofthrones", because our p-value proving it is 0.28.
<<<<<<< HEAD
=======

In the end, we cannot conclusively confirm if season 6 of the series *Game of Thrones* really lead to increased cluster activity and lasting relationships between two of the series main subreddits, but we can tentatively say it lead to an increase in their bonds and state that while there is decrease in inter-subreddit activity between "freefolk" and "gameofthrones", it is statistically not proven that the decrease stems from season 6's last episode being released.
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546

In the end, we cannot conclusively confirm if season 6 of the series *Game of Thrones* really lead to increased cluster activity and lasting relationships between two of the series main subreddits, but we can tentatively say it lead to an increase in their bonds and state that while there is decrease in inter-subreddit activity between "freefolk" and "gameofthrones", it is statistically not proven that the decrease stems from season 6's last episode being released.

 -->



<!--------------

### Sports

  Sports is something, which in the media depends heavily on an event-based schedule. The question which poses itself is always "When is the next championship?", "Did you see the Champions League final?" and "What do you do the next Super Bowl?", and this over many types of sports. But does this high saturation of "big" events drown out everything else, or can we still see a cluster-wide reaction on a specific sports competition?

  Let's begin with the biggest subreddits. For Europeans it may seem surprising that "nfl" is the top subreddit and decidedly not "soccer", or football as it is better known as. But, because Reddit was, and still is, mainly US American, the most [popular US sport](https://theenterpriseworld.com/most-popular-sports-in-the-usa/) is also dominant here. "soccer" is only third, after the in the US and Europe popular ice hockey subreddit. "cfb", "nfl_draft" and "oaklandraiders" are all football related and "mls" the north american soccer league subreddit.

  <figure id="fig-plot-top-subreddits-sports">
    <div class="plotly-embed-top">
      <iframe
        src="{{ 'assets/img/plots/top-subreddit-interaction-sports.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure ???.</strong> Top subreddits in the sports cluster by number of interactions.
    </figcaption>
  </figure>

  The popularity of american football is immediatly visible in both the [normalized temporal graph](#fig-normalized-weekly-sports) and the [sliding event intensity graph](#fig-sliding-event-intensity-sports). Every peak in the early parts of every year corresponds to the yearly Super Bowl, the final of the NFL league every year and a huge event in the US.

  <figure id="fig-normalized-weekly-sports">
    <div class="plotly-embed">
      <iframe
        src="{{ 'assets/img/plots/normalized_weekly_sports.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure ???.</strong> Hyperlink activities over time in the politics/news cluster.
    </figcaption>
  </figure>

  <figure id="fig-sliding-event-intensity-sports">
    <div class="plotly-embed">
      <iframe
        src="{{ 'assets/img/plots/sliding_event_intensity_sports.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure ???.</strong> Sliding event intensity in the politics/news cluster.
    </figcaption>
  </figure>

#### Super Bowl 2016 (February 2016)

  As the peaks are visible to such an extent, it would be interesting to see, if any other sport championship can even be noticed in our analysis. For this, we first have to establish the dominance of the Super Bowl. In the graph taking into account the hyperlink engagement [the year before and after](#fig-before-after-graph-super-bowl), there is a clear dominance of this event on February 2nd over any other events the same year.

  <figure id="fig-before-after-graph-super-bowl">
    <div class="plotly-embed-smallest">
      <iframe
        src="{{ 'assets/img/plots/before-after-comparison_sports_2016_02_07' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure ???.</strong> Activities the year before and after the 2016 Super Bowl.
    </figcaption>
  </figure>

  In terms of inter-subreddit relations, many links to subreddit showed only temporary connections. For example it's connection to "nflrountable" and "footballstrategy" disappeared nearly completely afterwards. It also stirred up emotions, an example being the improvement of emotional tone with the New Orleans team's subreddit "saints" and at the same time it also worsened it's tone with for example with the subreddit of San Francisco's team "49ers". 

  <figure id="fig-cluster-graph-super-bowl">
    <div class="plotly-embed">
      <iframe
        src="{{ 'assets/img/clusters/temporal_cluster_graph_superbowl.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure ???.</strong> Daily hyperlink activities around the 2016 Super Bowl.
    </figcaption>
  </figure>

  It would be possible to do a whole data analysis project only on the Super Bowl and how it is perceived on Reddit, but this is out of the scope of this project, as our goal here is to compare it to another event impacting the same cluster.

#### European Championships 2016 (June/July 2016)

  This other event is the UEFA European Championships 2016 in France. It took place from 10th of June to 10th of July. 

  <figure id="fig-cluster-graph-eu-championships">
    <div class="plotly-embed">
      <iframe
        src="{{ 'assets/img/clusters/temporal_cluster_graph_eu_championships.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure ???.</strong> Daily hyperlink activities around the European Championships 2016 in France.
    </figcaption>
  </figure>
  
  The [engagement graph of the year](#fig-before-after-graph-europe-cup-2016) shows what we already could have expected from the cluster wide temporal graph. There is no specific increase in activity in the whole cluster during the time of the championship. It even seems like the engagement decreased.

  <figure id="fig-before-after-graph-europe-cup-2016">
    <div class="plotly-embed-smallest">
      <iframe
        src="{{ 'assets/img/plots/before-after-comparison_sports_2016_06_25' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure ???.</strong> Activities the year before and after the European Championships 2016.
    </figcaption>
  </figure>

  One could only speculate for this decrease in engagement, but one reasonable theory seems to be the rational of why the championship is at the time it is. The theory being that during the summer, most big sports leagues are on pause, be that the NFL, NHL or the European football leagues. Having no club-based sports could concentrate the engagement into few subreddits or even halt it completely. This would be interesting to analyze, but unfortunately it is not possible with the current dataset. Looking again at the [sliding event intensity graph](#fig-sliding-event-intensity-sports), the decreasing engagement in the beginning of June can clearly be seen.

  The ego network of "soccer" reveals more or less what you'd expect. Similarly to the "nfl" subreddit, there are a lot of emotional shifts in relations with subreddits, for example a positive shift with "soccercirclejerk", a subreddit making fun of the main "soccer" subreddit, or a negative shift with Arsenal London's subreddit "gunners", though those shifts are not as strong as around the Super Bowl.

  It would also be possible to do a more extensive analysis on the European Championships and how it interacts with Reddit, especially taking into account the in Europe very popular local club seasons. Though this, like a possible study around the Super Bowl, is outside the scope of this project.
------>


<<<<<<< HEAD
---
### Take-away from intra-cluster analysis
Bringing together the intra-cluster analyses above, several clear patterns emerge that help explain how Reddit communities respond when the outside world intrudes.


### What We Learn from Inside the Clusters

1. **Big events trigger big reactions.**  
   The more universally important an event is, the stronger and more sustained the response within a cluster. The 2016 U.S. presidential election illustrates this vividly, with activity steadily intensifying in the lead-up to election day, followed by a pronounced and lasting drop in hyperlink activity once the event passed.

2. **Local importance does not guarantee global impact.**  
   Some events resonate powerfully within a narrow region of the network without reshaping the cluster as a whole. The release of *Pokémon GO* generated a clear surge of activity around **r/pokemongo**, yet this excitement remained largely localized and failed to propagate across the broader Gaming cluster.

3. **Event impact determines whether clusters respond.**  
   Not all events cross the threshold required to mobilize an entire cluster. The likelihood of a collective reaction increases with the perceived impact of the event, suggesting the existence of an implicit tipping point beyond which attention spreads beyond local neighborhoods and into the cluster at large.
=======
### Final takeaway
>>>>>>> 71078de2351d433e1f0bdd6f13d1cd52d54a3546

Considering all intra-cluster analysis done above, we may summarizes our findings:

1. Big events cause a big reaction. The bigger the importance of an event for everyone, the bigger the reaction. The 2016 US election clearly showcases this effect with continuously increasing activity up until the election and then a depression in hyperlink activity after.

2. Events can be important locally without affecting the whole cluster. The release of Pokémon Go showed a clear rise in activity around the "pokemongo" subreddit, but it's hype was not picked up by the whole cluster.

3. Event impact matters. The bigger the event impact, the more likely a reaction in a cluster will be. There seems to be an unquantified point at which the whole cluster picks up on an event.

4. Longer lasting events are hard, but not impossible to quantify, especially if their impact on a cluster is big.

All of those findings would make for interesting further analysis and deeper dives with more extensive datasets, but this is outside the scope of this project. We can certainly say that real-life events **do** have a measurable impact on Reddit and we can also say that event importance and length do play a role on how Reddit perceives them.
