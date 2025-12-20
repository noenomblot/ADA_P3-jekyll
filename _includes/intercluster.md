## When Events Ripple Through the Network

With the Reddit map now in hand, it is time to choose the moments that send shockwaves through both the real world and the digital one. To capture the diversity of collective attention, the events span multiple domains — from politics to gaming, from global sports to quiet holidays.

Some of these moments are impossible to forget. Others may have passed quietly, yet still left a mark on how communities interacted. The question is simple: **how did these events reshape Reddit’s social space?**

---

## Politics: When the World Holds Its Breath

Certain events pull political discussion into nearly every corner of the platform. The annexation of Crimea in March 2014 marked a sharp shift in global geopolitics and triggered sustained debate that extended far beyond explicitly political communities.  

The Brexit referendum in June 2016 produced a similar effect. As the United Kingdom voted to leave the European Union, discussions spilled across national, economic, and cultural boundaries. That same year, political attention reached a peak during the United States presidential election, an event that dominated Reddit in November 2016 and sparked intense, polarized conversations worldwide.

These moments did not just increase activity — they **reconfigured connections** between communities that rarely interacted before.

<div style="display: flex; justify-content: center; gap: 20px; margin: 20px 0;">
  <img src="assets/img/Crimee.jpg" width="250">
  <img src="assets/img/brexit.jpg" width="250">
  <img src="assets/img/election2016.png" width="250">
</div>
---

## Sports: A Global Crowd, One Conversation

Major sporting events have a unique ability to unite attention across borders. The opening of the 2014 FIFA World Cup in Brazil transformed Reddit into a global stadium, with discussions cutting across national and linguistic lines.  

This shared focus continued with Super Bowl XLIX in February 2015, a cultural milestone in the United States that drew in both sports and non-sports communities alike. The opening ceremony of the Rio de Janeiro Olympic Games in August 2016 extended this effect even further, concentrating global attention around a single, time-bound moment.

<div style="display: flex; justify-content: center; gap: 20px; margin: 20px 0;">
  <img src="assets/img/fifaWorldCup.jpg" width="250">
  <img src="assets/img/SuperBowl.jpg" width="250">
  <img src="assets/img/JO2016.jpg" width="250">
</div>
---

## Entertainment: Shared Stories, Shared Attention

Few things travel across Reddit as effortlessly as pop culture. The release of *Star Wars: The Force Awakens* in December 2015 reignited a legendary franchise and pulled together fans, critics, and casual viewers across dozens of communities.  

The film industry remained in focus during the 88th Academy Awards in February 2016, while television took center stage with the premiere of *Game of Thrones* Season 6 in April of the same year. These moments show how shared narratives can synchronize attention across otherwise unrelated spaces.

<div style="display: flex; justify-content: center; gap: 20px; margin: 20px 0;">
  <img src="assets/img/StarWars.png" width="250">
  <img src="assets/img/Oscars.jpg" width="250">
  <img src="assets/img/GOT6.jpg" width="250">
</div>
---

## Crises: Sudden Shocks, Emotional Surges

Not all events are anticipated. Some arrive abruptly, leaving behind sharp spikes in attention and emotion. The Ebola outbreak in West Africa in August 2014 escalated into a global health crisis, generating fear, uncertainty, and widespread discussion.  

Similarly, the terrorist attacks in Paris in November 2015 triggered waves of shock, grief, and international solidarity. Natural disasters follow a comparable pattern: the Illapel earthquake in Chile in September 2015 prompted immediate, emotionally charged responses as news spread across the platform.

These events compress time and space, briefly pulling distant communities into a shared emotional moment.

<div style="display: flex; justify-content: center; gap: 20px; margin: 20px 0;">
  <img src="assets/img/ebola.jpg" width="250">
  <img src="assets/img/bataclan.jpg" width="250">
  <img src="assets/img/ChileEarthquake.jpg" width="250">
</div>
---

## Holidays: Rhythms of Collective Life

Alongside singular events, recurring holidays provide a different lens on collective behavior. Independence Day in July 2014, Christmas Day in December 2015, and Thanksgiving in November 2016 represent predictable moments of cultural alignment.  

Rather than sudden shocks, these days reveal **rhythms** — how shared traditions subtly reshape online interaction year after year.

<div style="display: flex; justify-content: center; gap: 20px; margin: 20px 0;">
  <img src="assets/img/4july.jpg" width="250">
  <img src="assets/img/christmas.jpg" width="250">
  <img src="assets/img/Thanksgiving.jpg" width="250">
</div>
---

## Gaming: Digital Worlds, Real Impact

Finally, no exploration of Reddit would be complete without gaming. The release of *Pokémon GO* in July 2016 rapidly evolved into a global phenomenon, blending physical movement with digital play and spilling into communities far beyond gaming itself.  

Earlier, the PlayStation 4 release of *Grand Theft Auto V* in November 2014 extended the life of an already iconic title, while the reveal of the Nintendo Switch in October 2016 generated widespread anticipation for a new hybrid console.

These moments highlight how virtual worlds can trigger very real shifts in online attention.

<div style="display: flex; justify-content: center; gap: 20px; margin: 20px 0;">
  <img src="assets/img/PokemonGo.jpg" width="250">
  <img src="assets/img/GTAV.png" width="250">
  <img src="assets/img/Switch.jpg" width="250">
</div>
---

Together, these events form a diverse set of shocks — planned and unplanned, joyful and tragic, global and local. By tracing how each one ripples through Reddit, the platform becomes more than a collection of posts. It becomes a **sensor**, quietly recording how collective attention moves when the world changes.



## Reading the Ripple Effects at a Glance

The impact of major events is first examined at an aggregate level, grouping them by category to understand how highly salient real-world moments reshape activity across Reddit. When viewed through this lens, clear and structured patterns emerge.  

Political events stand out as the most disruptive overall, driving intense activity across Politics, World, News, and Technology communities. Their broad societal relevance pulls in audiences far beyond explicitly political spaces. Sporting events, by contrast, concentrate engagement within Sports while also activating World and Gaming communities, reflecting the global yet recreational nature of large competitions.  

Entertainment events generate strong activity in Entertainment and Gaming, with noticeable spillover into World-oriented discussions, underscoring their cultural reach beyond core fan bases. Social and natural disasters produce sharp engagement spikes in World and Social communities, revealing a collective focus on information sharing and social response during moments of crisis. Holidays, meanwhile, display a far more diffuse and subdued pattern. While widely observed, they rarely provoke concentrated bursts of discussion within specific communities.

  <figure id="fig-plot-top-subreddits-politics">
    <div class="plotly-embed-smaller">
      <iframe
        src="{{ 'assets/img/plotly_plots/inter_category_heatmap_elegant.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure 5.</strong> Inter-category interaction heatmap showing the intensity of interaction of cluster per event category.
    </figcaption>
  </figure>
---

## How Events Reshape Connections and Sentiment

Beyond sheer posting volume, these events also leave distinct structural footprints on the Reddit network by altering how communities connect to one another — and how those interactions feel.

Political events, in particular, tend to **intensify existing relationships rather than create new ones**. During these periods, the number of hyperlinks exchanged between clusters nearly doubles and often remains elevated even after the event window closes. This persistence suggests a lasting reinforcement of interaction pathways. Notably, this surge in connectivity does not correspond to a rise in positive sentiment. Discussions remain, on average, emotionally neutral, highlighting how increased engagement can amplify debate without necessarily improving tone.

Sporting events follow a similar but more transient trajectory. Interactions between Sports, World, and Gaming communities strengthen noticeably during the event window, only to gradually return to baseline within a few months. Despite their temporary nature, these events are accompanied by a clear uptick in positive sentiment, pointing to a more unifying and emotionally uplifting form of collective engagement.

Entertainment events occupy a middle ground. While they increase the overall volume of hyperlinks exchanged, they do not consistently reshape the network’s structure. Strengthened and weakened ties tend to balance out, and sentiment shifts show no strong directional bias. The result is a surge in activity without lasting structural consequences.

Social and natural disasters tell a different story. These events are more likely to **strain connections** than reinforce them. Even some of the strongest links — particularly between World and Social communities — weaken immediately following such shocks. This structural fragmentation aligns with predominantly negative sentiment shifts, reflecting the distressing and emotionally charged nature of these crises.

Holidays leave only a faint structural imprint. Few connections show temporary strengthening, and overall interaction patterns remain largely unchanged. Yet sentiment tells a warmer story: these periods are associated with broadly positive emotional shifts, suggesting that holidays subtly improve tone even if they do not reorganize attention.

Gaming events stand apart due to the central position of the Gaming community itself. While interactions among non-gaming clusters remain relatively stable, links involving Gaming experience pronounced strengthening, occasionally punctuated by sharp weakening. Overall, these events coincide with increased positive sentiment across the network, reinforcing gaming’s role as a powerful and emotionally engaging driver of collective attention on Reddit.

Taken together, these patterns reveal that not all events ripple through the network in the same way. Some reinforce long-standing pathways, others briefly synchronize attention, and a few fracture connections entirely — each leaving a distinct signature in how Reddit responds when the world changes.





<figure class="figure text-center">
  <img src="assets/img/averageSentiment.png"
       alt="Average sentiment shift by event category"
       width="750">
  <figcaption class="figure-caption">
    <strong>Figure 6.</strong> Average sentiment shift observed across Reddit
    communities for each event category. Positive values indicate an overall
    increase in sentiment, while negative values reflect predominantly adverse
    emotional responses. Natural and social disasters stand out as the only event
    category associated with a net negative sentiment shift.
  </figcaption>
</figure>

<figure class="figure text-center">
  <img src="assets/img/strengthenedWeakenedInterConnections.png"
       alt="Strengthened versus weakened inter-community connections by event category"
       width="750">
  <figcaption class="figure-caption">
    <strong>Figure 7.</strong> Number of strengthened and weakened inter-community
    connections by event category. Political events primarily reinforce existing
    connections, whereas natural and social disasters are associated with a higher
    prevalence of weakened ties. Other event categories exhibit more balanced
    structural effects.
  </figcaption>
</figure>


## Event-Born Links: Short Flares or Lasting Imprints?

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
