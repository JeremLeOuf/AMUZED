---
description: We are using a concept called L3 security
---

# Security

![](<../../.gitbook/assets/Screenshot 2022-01-18 at 12.15.40.png>)

**AMUZED has partnered with Venly for the AMUZED wallet solution. Venly has three layers of security:**

**First layer,** _core blockchain characteristics._\
Every user’s assets live on the corresponding blockchain, and thus inherit all the underlying blockchain’s security benefits.

**Second layer**, _securing the private key of a user’s wallet._\
The first part is encrypting the private key with a Keystore and a password, an extremely long password, this is done via AES 128-bit encryption. Next, we take the password and split it into 3 parts using the[ Shamir Secret Sharing](https://en.wikipedia.org/wiki/Shamir's\_Secret\_Sharing) algorithm. The part that belongs to the user is then encrypted for the 2nd time using AES 128, using the user's pin code. Once that is done all three parts are stored in a vault where they are encrypted for a 3rd or 2nd time. Access control policies provide strict control over who can access the vaults and what part of the key and which permission they have. On top of those policies, we’ve also added additional ACLs ([Access Control Lists](https://en.wikipedia.org/wiki/Access\_control\_list)) to control access on the application and infrastructure level.

**Third layer**, _abstracting the use of a user’s private key._\
On top of the layer 2 encryption, we add the need for a pin code, if an attacker would be able to bypass all our different levels of security and is able to decrypt and assemble the different parts of the private key, he would still need to know the user's pin code to gain access to the user’s assets. Additionally, we allow users to set a different pin code for each wallet they own, making it even harder for an attacker to get away with all the user’s valuables.



