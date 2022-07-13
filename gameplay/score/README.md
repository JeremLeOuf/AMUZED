# Score

#### The AMUZED Score is calculated for each artist using an algorithm that takes into account real-life data points

![](../../.gitbook/assets/Score\_Result.png)

### Score Logic

The AMUZED Score captures the real-life performance of any music artist over a given timeframe (usually a week). The score aims to be a "snapshot" of the current situation and takes into account absolute as well as relative data. That way not only the total level of fame, but also the current trend and sentiment gets taken into account. In general for artists scores: More Fame = More Points / Currently Trending = More Points&#x20;

### Score Parameters&#x20;

There are 89 data points that AMUZED tracks for any artists and that serve as input parameters for the scoring algorithm. These data points cover the most important stats around music, media, and public life. These data points can be categorised into two main categories:&#x20;

<details>

<summary>Music  Data </summary>

* Spotify Data
* Deezer Data&#x20;
* Soundcloud
* Bandsintown Data

</details>

<details>

<summary>Social  Data</summary>

* Google Trends
* Instagram Data
* Facebook Data&#x20;
* Youtube Data
* Twitter Data
* Twitch Data&#x20;
* TikTok Data
* Wikipedia Data

</details>

As it is time-consuming and inefficient to get all of the input parameters by ourselves, AMUZED has partnered up with [Chartmetric](https://chartmetric.com/) (Data Provider) to provide up-to-date data for any artists. AMUZED is using their API access for the input, while developing the algorithm for the actual scoring in-house.&#x20;

### Score Algorithm

The score algorithm takes all of the relevant data points in a given timeframe (usually 6 days) and applies different functions to them.&#x20;

In a nutshell: The data points are compared across all artists in a variety of ways and afterwards normalised. Furthermore, the different data points are weighted by the scoring algorithm. Generally speaking, music streaming data has the biggest weights as it is the main aspects of any artists performance.&#x20;

### Natural Score

The scoring algorithm outputs a "natural score" of 0 - 100 for every artist for a given period of time, whereas 100 is the highest score that can be achieved.&#x20;

Without Bonus (XP/Rarity/Headliner), the "natural score" can not be higher than 100.&#x20;

### Score Bonus

The natural score for any token can get multiplied by different bonus factors that are individual to each token. The three multipliers are: [Experience](experience-bonus.md) (E), [Rarity](rarity-bonus.md) (R), [Headliner](headliner-bonus.md) (H) and they are multiplied with the natural score (N) to give us the final score (F) for a tournament week according to the following formula:&#x20;

$$
F= N * (1+(E*R+H))
$$

* E can have a range of 0 to 12.5% depending on the experience level
* R can have a range of 1 to 4 depending on the rarity of the token
* H is binary either 0 or 5%

{% hint style="info" %}
**Example**:&#x20;

Let's take a platinum token of an artist with an experience level of 4 that is the headliner and with a natural score of 75:

Final Score = 75 \*(1+(5.5%\*3+5%))

Final Score = 91.125&#x20;

This token would have a final score of 91.125 points - a very good performance
{% endhint %}

{% hint style="success" %}
**Highest Score possible:**&#x20;

The highest score that can be achieved is 155

This would be a _Diamond_ token with _XL_=10 that is selected as a _Headliner_ and on top of that has a _natural score_ performance of 100

100\*(1+(12.5%\*4+5%)) = **155 points**
{% endhint %}
