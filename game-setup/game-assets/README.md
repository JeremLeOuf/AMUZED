# Game Assets

The AMUZED Game can only be played by using in-game assets. These in-game assets are digital trading cards each representing a music artist. The tokens can be differentiated between **authenticated tokens** (actual NFTs) that are bought by users on the [primary](../../marketplace/primary-marketplace/) and [secondary](../../marketplace/secondary-marketplace.md) marketplace, and **free tokens** (not NFTs) that are distributed to each new user when signing up.&#x20;

### Authenticated Tokens

For each music artist that AMUZED is working with, limited edition collectible tokens based on the concept of NFTs are created. These non-fungible tokens are part of the blockchain ecosystem and thus cannot be deleted, copied, stolen or modified. In addition, the owner of each token can be uniquely and transparently identified. They are therefore forgery-proof, unique digital tokens for eternity, with an owner entitled to decision-making power about his or her own tokens.&#x20;

**In total there are 1111 tokens that are created for every artist**&#x20;

These 1111 tokens are split between 4 different categories:

![Overview of AMUZED token categories: Glass, Gold, Platinum, Diamond (left to right)](../../.gitbook/assets/Tokens.png)

* <mark style="color:red;">**Glass**</mark> (**1000** editions per artist)
* <mark style="color:yellow;">**Gold**</mark> (**100** editions per artist)
* <mark style="color:green;">**Platinum**</mark> (**10** editions per artist)
* <mark style="color:purple;">**Diamond**</mark> (**1** edition per artist)

Each of these NFTs has a unique serial number on the front (top right), so that the user can clearly differentiate between tokens from the same artist and same rarity.

On the Smart Contract side, the tokens are based on the ERC-721 standard, which is a Non-Fungible Token Standard that implements an API for tokens within Smart Contracts. In order to be defined as an ERC-721 token, the following methods and events must be included in the underlying smart contract:&#x20;

#### **Methods in the ERC-721 Standard**

```
//  function balanceOf(address _owner) external view returns (uint256);
    function ownerOf(uint256 _tokenId) external view returns (address);
    function safeTransferFrom(address _from, address _to, uint256 _tokenId, bytes data) external payable;
    function safeTransferFrom(address _from, address _to, uint256 _tokenId) external payable;
    function transferFrom(address _from, address _to, uint256 _tokenId) external payable;
    function approve(address _approved, uint256 _tokenId) external payable;
    function setApprovalForAll(address _operator, bool _approved) external;
    function getApproved(uint256 _tokenId) external view returns (address);
    function isApprovedForAll(address _owner, address _operator) external view returns (bool);
```

#### Events **in the ERC-721 Standard**

```
// event Transfer(address indexed _from, address indexed _to, uint256 indexed _tokenId);
    event Approval(address indexed _owner, address indexed _approved, uint256 indexed _tokenId);
    event ApprovalForAll(address indexed _owner, address indexed _operator, bool _approved);
```

### Common Tokens

In addition to the actual NFTs, which are limited to a number of 1111 tokens per artist, there will be an **unlimited number of free common cards** per artist that can be attributed to new users, in order to facilitate free and easy onboarding to the AMUZED manager game.
