# Currency - ETH

The currency that is used on the AMUZED platform is ETH. This means that not only the prices on the platform are denoted in ETH/EUR or ETH/USD, but also the actual exchange is happening in ETH (ETH is transferred out of and into the users AMUZED wallet).&#x20;

{% hint style="info" %}
To be specific: As the whole AMUZED platform is built on the Polygon Network but the currency of exchange is not MATIC but ETH, the actual exchange happens ins Wrapped Ether ([WETH](https://polygonscan.com/token/0x7ceb23fd6bc0add59e62ac25578270cff1b9f619)). WETH is a one to one representation of ETH and is built on the ERC20 token standard, which basically allows us to trade with ETH with the upsides of the polygon chain (i.e. lower gas fess and fast transaction times).&#x20;

However, the gas fees for the transactions need to be paid in MATIC. Therefore, in the standard case a user wallet would have to hold both ETH and MATIC in order to do transactions. AMUZED is going the extra mile to avoid this for the user and actually pays for ALL of the gas fees on the AMUZED platform, which enhances the user experience drastically. AMUZED uses a [Gas Tank](../matic-gas-tank.md) for this.&#x20;
{% endhint %}

There are two main ways to deposit ETH into the AMUZED Wallet:&#x20;

(Better for Crypto Newbies)

{% content-ref url="ramp-on.md" %}
[ramp-on.md](ramp-on.md)
{% endcontent-ref %}

(For users familiar with Crypto and non-custodial wallets)

{% content-ref url="metamask.md" %}
[metamask.md](metamask.md)
{% endcontent-ref %}

