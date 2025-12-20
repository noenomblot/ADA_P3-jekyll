## 5. Zooming into Events and Communities 

chord
<div class="flourish-embed flourish-chord" data-src="visualisation/26916041">
  <script src="https://public.flourish.studio/resources/embed.js">
  </script>
  <noscript>
    <img src="https://public.flourish.studio/visualisation/26916041/thumbnail" width="100%" alt="chord visualization" />
  </noscript>
</div>



Storyline: 
* Show US elections as an example on how the cluster reacts and how it works (1 case, US elections)
* Show difference between big and small event (2 cases, Terrorism)
* Show difference between american and non-american event (2 cases, Sports)
* Show difference between long and short event of similar "importance" (2 cases, Entertainment)
* So small events can't ever do anything? (1 case; Pokemon Go)

### If a big event happens, how do clusters react? - US Presidential Election 2016

  In the politics/news cluster, the biggest subreddits in terms of subreddit interactions are unsurprisingly political. The biggest being "the_donald" a right wing, now banned, subreddit supporting Donald Trump especially during the 2016 US presidential election. The second biggest is "conspiracy" and the third and fourth "politics" and "news", two subreddits also strongly involved in the US election cycle of 2016. It has to be noted that "politics" and "news" tend to be anti-Trump and are taken as "the_donald"s counter-pole in our analysis.

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

  We may even statistically capture this increase in posts. If our hypothesis is that an increase of hyperlink connections between "politcs" and "the_donald" is due to an event with our null hypothesis being that this is not the case, we may do a t-test during the run-up of the election and evaluate it's p-value. On the date of the election, we obtain a p-value of 0.081. While this is not decisive, it strongly indicates a statistical correlation between the event and the increase in hyperlink connections.

  Using the same methodology between the subreddits "the_donald" and "conspiracy", an even stronger evidence is obtained. The p-value is 0.034, a value which lets us completely reject the null hypothesis. For both relations there is a statistically shown low stability of connections. Which, again considering the "post-election" collapse, makes sense. At least for a short moment, people distanced themselves from politics.

  The pause does not last though. The connections forged during the elections are here to stay. The links from "the_donald" with "politics" due to the election fade very slowly with a statistical half life of the connection being 55 weeks. This is very long, for comparison, the half life between "the_donald" and "news" is 22 weeks. In the case of "conspiracy" and "the_donald", the connection does not even decay, but rather increase in the weeks following. A trend well reflected in real life during both of Donald Trump's periods in office.


---

### Do smaller events evoke a similar reaction? - Release of *Pokémon Go*

  In the case of the US election, we saw an important, if not the most important, event on Reddit which culminates in an enormous, cluster wide reaction. Now it is only pertinent to ask, how Reddit's reaction to something more niche would be. For this, we will look at the release of the augmented reality mobile game *Pokémon Go*. The subreddits important for this event are called "pokemon" and "pokemongo", both situated in the Gaming cluster. With 621 hyperlink interactions during the period of the available dataset and thus the 32nd most important subreddit within the cluster, the subreddit "pokemongo" could still be counted as one of the more important ones. This is especially considering the subreddit becoming active only after the game's release in June 2016, i.e. in only the second half of the data acquisition period.


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


  A big reason for why a subreddit created in 2016 can still be in the top 50, is the more or less unique development the pokemongo community followed: Instead of only being organized in a global subreddit, almost immediately regional groups were formed. This makes sense for a game which, [before Covid](https://www.gamedeveloper.com/design/how-i-pokemon-go-i-evolved-in-response-to-the-covid-19-pandemic){:target="_blank"}, was a decentralized/local game with multiplayer aspects. In figure [figure ???](#fig-cluster-graph-pokemongo) the daily development around the worldwide releases in June can be followed. Highlighted are the main subreddit "pokemongo", the subreddit "pokemon" and various regional offshoot relating to either of them.

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

The observations from the temporal clustering graph can also be shown in [figure ???](#fig-before-after-graph-charlie-hebdo), which shows the average number of hyperlink connections in the year before, the year after and the days around the incident. There is no significant increase of hyperlink connections visible in the Geography/World cluster.


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

Looking more carefully at the relationship of the subreddits "france" and "paris", we may deduce a newly (re-) formed but temporary relationship between the two, due to the event on January 7th. This being said, the connections between the two subreddits are sparse and far between, but those which do occur predominantly convey positive and supportive sentiments.

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

While these events are first and foremost human tragedies, this analysis shows how the magnitude of an incident is important in how big Reddit's reaction becomes. Though this being said, both attacks are tragedies and Reddit's reaction should not, and does not, quantify the real loss of life in any way. If anything, these patterns suggest that in moments of large-scale human catastrophe, inter-community engagement on Reddit is more often driven by expressions of empathy than by sustained structural change.

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

### Can Longer Lasting Events be Distinguished? - Release of Season 6 of *Game of Thrones*

We come to a topic, which at the time was highly celebrated, but now in hindsight many consider the [beginning of the downfall](https://www.reddit.com/r/gameofthrones/comments/xa3t7d/why_do_people_now_include_season_6_along_7_8_as/) of the popular TV-Series *Game of Thrones*. Due to the nature of the serial release, usually episodes do not air at the same time, but usually are published in a weekly frequency. As such, we would not expect an event, even of the cultural impact of *Game of Thrones* to show up on a temporal graph. 

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

Now the logical follow up question would be to see the values after the release of the last of season 6's episodes on June 26th.Indeed, we a decay in activity between the two subreddits "freefolk" and "gameofthrones". This decay however is quite a bit smaller, for Cohen's d being -0.374 and here we can clearly reject the hypothesis of the last episode of the season causing a break of previously forged bonds between "freefolk" and "gameofthrones", because our p-value proving it is 0.75, 

We cannot conclusively confirm if season 6 of the series *Game of Thrones* really lead to increased cluster activity and lasting relationships between two of the series main subreddits, but we can tentatively say it lead to an increase in their bonds and clearly state there is no discernable decrease after the season ended.





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





### Final takeaway



