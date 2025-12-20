## When Events Ripple Through the Network

With the Reddit map now in hand, it is time to choose the moments that send shockwaves through both the real world and the digital one. To capture the diversity of collective attention, the events span multiple domains — from politics to gaming, from global sports to quiet holidays.

Some of these moments are impossible to forget. Others may have passed quietly, yet still left a mark on how communities interacted. The question is simple: **how did these events reshape Reddit’s social space?**

---

## Politics: When the World Holds Its Breath

Certain events pull political discussion into nearly every corner of the platform. The annexation of Crimea in March 2014 marked a sharp shift in global geopolitics and triggered sustained debate that extended far beyond explicitly political communities.  

The Brexit referendum in June 2016 produced a similar effect. As the United Kingdom voted to leave the European Union, discussions spilled across national, economic, and cultural boundaries. That same year, political attention reached a peak during the United States presidential election, an event that dominated Reddit in November 2016 and sparked intense, polarized conversations worldwide.
<div style="text-align: center; margin: 2rem 0;">
  <img src="assets\img\events\politics.png">
</div>

These moments did not just increase activity — they **reconfigured connections** between communities that rarely interacted before.

---

## Sports: A Global Crowd, One Conversation

Major sporting events have a unique ability to unite attention across borders. The opening of the 2014 FIFA World Cup in Brazil transformed Reddit into a global stadium, with discussions cutting across national and linguistic lines.  

This shared focus continued with Super Bowl XLIX in February 2015, a cultural milestone in the United States that drew in both sports and non-sports communities alike. The opening ceremony of the Rio de Janeiro Olympic Games in August 2016 extended this effect even further, concentrating global attention around a single, time-bound moment.

<div style="text-align: center; margin: 2rem 0;">
  <img src="assets\img\events\sports.png">
</div>
---

## Entertainment: Shared Stories, Shared Attention

Few things travel across Reddit as effortlessly as pop culture. The release of *Star Wars: The Force Awakens* in December 2015 reignited a legendary franchise and pulled together fans, critics, and casual viewers across dozens of communities.  

The film industry remained in focus during the 88th Academy Awards in February 2016, while television took center stage with the premiere of *Game of Thrones* Season 6 in April of the same year. These moments show how shared narratives can synchronize attention across otherwise unrelated spaces.
<div style="text-align: center; margin: 2rem 0;">
  <img src="assets\img\events\movies.png">
</div>
---

## Crises: Sudden Shocks, Emotional Surges

Not all events are anticipated. Some arrive abruptly, leaving behind sharp spikes in attention and emotion. The Ebola outbreak in West Africa in August 2014 escalated into a global health crisis, generating fear, uncertainty, and widespread discussion.  

<div style="text-align: center; margin: 2rem 0;">
  <img src="assets\img\events\social.png">
</div>

Similarly, the terrorist attacks in Paris in November 2015 triggered waves of shock, grief, and international solidarity. Natural disasters follow a comparable pattern: the Illapel earthquake in Chile in September 2015 prompted immediate, emotionally charged responses as news spread across the platform.

These events compress time and space, briefly pulling distant communities into a shared emotional moment.


---

## Holidays: Rhythms of Collective Life

Alongside singular events, recurring holidays provide a different lens on collective behavior. Independence Day in July 2014, Christmas Day in December 2015, and Thanksgiving in November 2016 represent predictable moments of cultural alignment.  

Rather than sudden shocks, these days reveal **rhythms** — how shared traditions subtly reshape online interaction year after year.

<div style="text-align: center; margin: 2rem 0;">
  <img src="assets\img\events\holidays.png">
</div>
---

## Gaming: Digital Worlds, Real Impact

Finally, no exploration of Reddit would be complete without gaming. The release of *Pokémon GO* in July 2016 rapidly evolved into a global phenomenon, blending physical movement with digital play and spilling into communities far beyond gaming itself.  

Earlier, the PlayStation 4 release of *Grand Theft Auto V* in November 2014 extended the life of an already iconic title, while the reveal of the Nintendo Switch in October 2016 generated widespread anticipation for a new hybrid console.

<div style="text-align: center; margin: 2rem 0;">
  <img src="assets\img\events\games.png">
</div>

These moments highlight how virtual worlds can trigger very real shifts in online attention.

---

Together, these events form a diverse set of shocks — planned and unplanned, joyful and tragic, global and local. By tracing how each one ripples through Reddit, the platform becomes more than a collection of posts. It becomes a **sensor**, quietly recording how collective attention moves when the world changes.



## Reading the Ripple Effects at a Glance

The impact of major events is first examined at an aggregate level, grouping them by category to understand how highly salient real-world moments reshape activity across Reddit. When viewed through this lens, clear and structured patterns emerge.  

Political events stand out as the most disruptive overall, driving intense activity across Politics, World, News, and Technology communities. Their broad societal relevance pulls in audiences far beyond explicitly political spaces. Sporting events, by contrast, concentrate engagement within Sports while also activating World and Gaming communities, reflecting the global yet recreational nature of large competitions.  

Entertainment events generate strong activity in Entertainment and Gaming, with noticeable spillover into World-oriented discussions, underscoring their cultural reach beyond core fan bases. Social and natural disasters produce sharp engagement spikes in World and Social communities, revealing a collective focus on information sharing and social response during moments of crisis. Holidays, meanwhile, display a far more diffuse and subdued pattern. While widely observed, they rarely provoke concentrated bursts of discussion within specific communities.

  <figure id="fig-intercategory-heatmap">
    <div class="plotly-embed-heatmap">
      <iframe
        src="{{ 'assets/img/plotly_plots/inter_category_heatmap_elegant.html' | relative_url }}"
        loading="lazy">
      </iframe>
    
  </div>
  <figcaption>
    <strong>Figure X.</strong> Inter-category interaction heatmap.
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

 <figure id="fig-plot-conn">
    <div class="plotly-embed-bar">
      <iframe
        src="{{ 'assets/img/plotly_plots/strengthened_vs_weakened_connections.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure 5.</strong> Number of strengthened and weakened inter-community
    connections by event category.
    </figcaption>
  </figure>

  <figure id="fig-plot-sentiment">
    <div class="plotly-embed-bar">
      <iframe
        src="{{ 'assets/img/plotly_plots/sentiment_shift_barplot.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      </strong> Figure 7.</strong> Average sentiment shift observed across Reddit
    communities for each event category.
    </figcaption>
  </figure>




## Zooming In: When Communities React Together

To truly understand how Reddit functions as a social system, it is not enough to look only at global trends. The real insight emerges when attention shifts to **pairwise relationships** — how two communities respond *together* when the world changes. These interactions reveal whether connections are reactive, insulated, or mutually reinforcing.

A natural place to begin is the political segment of Reddit. Political discourse often leaks into other domains, yet at times remains surprisingly contained. Which of these outcomes occurs depends heavily on the nature of the event.

---

### Politics Meets Entertainment: One-Way Spillover

The relationship between political and entertainment communities reveals a clear asymmetry. During the 2016 U.S. presidential election, interactions between these clusters increase noticeably. Hyperlinks surge following the event and remain elevated well beyond the immediate aftermath. Politically charged moments pull entertainment communities into the conversation — through satire, commentary, late-night humor, or media framing — leaving behind a lasting imprint on their connection.

The reverse, however, does not hold. When *Star Wars: The Force Awakens* was released, one of the most anticipated entertainment events of the decade, political communities remained largely unmoved. No comparable spike in interaction appears, and ties between the two clusters do not strengthen. Cultural moments may dominate attention, but they rarely redirect political discourse. This pattern reveals a **one-directional spillover**, where politics extends outward, while entertainment remains self-contained.

 <figure id="fig-plot-top-subreddits-politics">
    <div class="plotly-embed-long">
      <iframe
        src="{{ 'assets/img/plotly_plots/graph1_4.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure 5.</strong> Posting trend between the Politics community and the Entertainment community around the US elections of 2016.
    </figcaption>
  </figure>

  <figure id="fig-plot-top-subreddits-politics">
    <div class="plotly-embed-long">
      <iframe
        src="{{ 'assets/img/plotly_plots/graph4_1.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure 5.</strong> Posting trend between the Politics community and the Entertainment community around the release of "The Force Awakens".
    </figcaption>
  </figure>
---

### Politics and Sports: Parallel Worlds

A very different picture emerges when politics intersects with sports. Examining interactions around the 2015 Super Bowl shows remarkable stability. Posting behavior remains consistent before and after the event, and hyperlink exchange does not display any sustained change.

Despite their shared visibility in public life, political and sports communities largely operate in parallel. Major sporting events generate intense internal engagement, yet they do not meaningfully cross into political discussion in a lasting way. This pairing illustrates **parallel coexistence** — two communities occupying the same platform, reacting to the world independently, and rarely influencing one another.

 <figure id="fig-plot-top-subreddits-politics">
    <div class="plotly-embed-long">
      <iframe
        src="{{ 'assets/img/plotly_plots/graph1_9.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure 5.</strong> Posting trend between the Politics community and the Sports community around the US elections of 2016.
    </figcaption>
  </figure>

  <figure id="fig-plot-top-subreddits-politics">
    <div class="plotly-embed-long">
      <iframe
        src="{{ 'assets/img/plotly_plots/graph9_1.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure 5.</strong> Posting trend between the Politics community and the Sports community around the 2015 Superbowl.
    </figcaption>
  </figure>
---

### Politics and Social Communities: Mutual Amplification

The strongest coupling appears between political and social communities. Both the 2016 U.S. election and the November 2015 Paris terrorist attacks trigger pronounced, synchronized reactions. Political events lead to heightened interaction with social communities as discussions around identity, values, and collective response intensify. At the same time, socially defined crises provoke political engagement, producing similar peaks in activity.

In both directions, interactions strengthen around moments of shared concern and remain elevated beyond the event window. This bidirectional sensitivity reflects **mutual amplification** — a relationship where engagement in one domain actively reinforces engagement in the other whenever events blur the line between social experience and political interpretation.

 <figure id="fig-plot-top-subreddits-politics">
    <div class="plotly-embed-long">
      <iframe
        src="{{ 'assets/img/plotly_plots/graph1_18.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure 5.</strong> Posting trend between the Politics community and the Social community around the US elections of 2016.
    </figcaption>
  </figure>




  <figure id="fig-plot-top-subreddits-politics">
    <div class="plotly-embed-long">
      <iframe
        src="{{ 'assets/img/plotly_plots/graph18_1.html' | relative_url }}"
        loading="lazy">
      </iframe>
    </div>
    <figcaption>
      <strong>Figure 5.</strong> Posting trend between the Politics community and the Social community around the Paris attacks of 2015.
    </figcaption>
  </figure>
---

## A Digital Mirror of Real Social Life

Taken together, these patterns closely echo dynamics observed in the real world. Not every group responds to the same events, and not every interaction carries equal influence. Some communities are tightly interwoven, with reactions that ripple across boundaries. Others influence one another asymmetrically, while some coexist with little interaction at all, just like in the real world.

Reddit, then, is not a uniformly reactive system. It is a mosaic of social spheres, where connections strengthen, weaken, or remain untouched depending on context. In this way, the platform mirrors human society itself — selective, uneven, and shaped as much by shared meaning as by shared space.


