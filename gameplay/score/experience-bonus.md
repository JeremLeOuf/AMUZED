# Experience Bonus

**Individual tokens can earn Experience Points (XP) to level up in their Experience Levels (XL) when they are used in AMUZED weekly tournaments**

![](../../.gitbook/assets/Token\_XP.png)

#### Experience Levels (XL)

For each token there are **10 Experience Levels** to which the individual token can level up to, in order to gain additional % bonuses on the "natural score" that is given to an artist. For each level there are different bonus percentages that are applied to the score:

| Experience Level | Bonus % |
| ---------------- | ------- |
| Level 1          | 2.5%    |
| Level 2          | 3.5%    |
| Level 3          | 4.5%    |
| Level 4          | 5.5%    |
| Level 5          | 6.5%    |
| Level 6          | 7.5%    |
| Level 7          | 8.5%    |
| Level 8          | 9.5%    |
| Level 9          | 10.5%   |
| **Level 10**     | 12.5%   |

{% hint style="info" %}
The bonus percentage for XL gets multiplied to the weekly "natural score" for that specific token.&#x20;

Example:&#x20;

If a glass token has a "natural performance score" of 100 and has XL=5, then the total score is equal to 100\*1.055 = 105.5 Points
{% endhint %}

#### Experience Points (XP)

In order for token to get to the next experience level (XL) they need to accumulate experience points (XP) during the weekly tournaments. Each time a token is used within the game, it generates XP as follows:&#x20;

$$
XP = B + (L*0.15)+ (H*25)
$$

* **B** denotes the "Base XP" that every token gets when it is played. The Base XP is fixed at 50 points&#x20;
* **L** denotes the lineup score. Logically, the token "learns" from the other artists in the lineup. The Lineup score will get multiplied by 15% to earn XP for the individual token.&#x20;
* **H** is the variable for "Headliner". It is a binary variable (0 or 1). If the specific token is the headliner in its lineup, then the variable is = 1. If the token is not the headliner the variable is = 0. The variable is multiplied by 25.&#x20;

In order to level up, the token needs to collect enough XP. A classical learning curve is usually steeper in the beginning before the marginal rate of return diminishes. This logic is also applied in the XP system, as it gets increasingly more difficult with each level to level up:&#x20;

| XP Achieved | Experience Level |
| ----------- | ---------------- |
| 150         | Level 1          |
| 300         | Level 2          |
| 500         | Level 3          |
| 1000        | Level 4          |
| 1600        | Level 5          |
| 2300        | Level 6          |
| 3100        | Level 7          |
| 4000        | Level 8          |
| 5000        | Level 9          |
| 7000        | Level 10         |

{% hint style="warning" %}
When a token is sold on the secondary marketplace, only the experience level (XP) is secure, whereas all of the experience points up to that level are lost and have to be earned again.&#x20;

Example:&#x20;

When a token has an experience level of 4 and has currently 1520 XP but is sold on the secondary marketplace, then the new owner will receive the token with XL = 4 and XP=1000, as the 520 additional XP are lost.&#x20;
{% endhint %}
