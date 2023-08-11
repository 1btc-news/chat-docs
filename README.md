# 1btc Chat

## Introduction

{% hint style="info" %}
**1btc Chat is a unique community designed specifically for Bitcoin holders who possess at least 1 BTC.**
{% endhint %}

This platform aims to bring together this exclusive group, leveraging their strong value signal and enabling them to collaborate and shape their own narrative.

## Mission

Our mission is to expand and protect human sovereignty.

## Comparison with other platforms

The 1btc Chat platform sets itself apart from other social platforms like Discord and Telegram, which typically employ traditional authentication methods.

Instead, 1btc Chat adopts a wallet-first approach, where users' cryptocurrency address serves as their identity within the chat. This approach allows for pseudonymity while prioritizing privacy and security.

## Verifying a 1btc Holder

To ensure the authenticity of the community, it is crucial to verify that a user possesses at least 1 BTC. This verification process involves the following steps:

1. [**Connect a Wallet:**](verification/connect-wallet.md) Connect with either a [Hiro](https://wallet.hiro.so/wallet/install-web) or [Xverse](https://www.xverse.app/) wallet, used to to generate the required signatures and determine the dust address for verification.
2. [**Designate BTC:**](verification/designate-btc.md) Create a separate account for the balance used to verify in the wallet of your choice, then transfer a little more than 1 BTC to cover transaction fees. This Bitcoin cannot be spent or access will be lost.
3. [**Sign a Message:**](verification/sign-message.md) Sign a message from the 1btc API to prove ownership of the Hiro/Xverse wallet, which in turn will generate a unique Bitcoin address for verifying the balance.
4. [**Send Dust Transaction:**](verification/send-dust.md) Send a minimal amount of Bitcoin from the address with more than 1 BTC to the unique, generated BTC address. This amount is commonly referred to as "dust" and equal to 0.00006 BTC or 6,000 satoshis.\
   <mark style="color:orange;">**Note: nobody has access to this dust address, and the dust will not be returned.**</mark>
5. **Await Verification:** The API actively monitors the generated BTC address for receiving the dust transaction. Upon successful receipt of the dust, the API verifies the user's account balance and marks it as verified.\
   <mark style="color:orange;">**Note: if the user spends Bitcoin from the address, their verified status will be revoked, resulting in the loss of access to the chat.**</mark>

## Security and Privacy

1btc Chat places the utmost importance on security measures. The utilization of a dust transaction ensures that the user's funds remain securely stored in their primary wallet. Furthermore, the adoption of a separate wallet for the login account minimizes the risk of compromising the user's funds. Users are strongly advised to review and verify all transactions to ensure their security.

Nevertheless, it is essential to acknowledge privacy concerns. Bitcoin transactions are inherently traceable, which can potentially compromise user identities. To address these concerns, users can consider transferring their Bitcoin to and from exchanges or implementing privacy-enhancing techniques such as CoinJoin.

## Independent Verification and API Usage

The transparency and integrity of the 1btc Chat community are further reinforced through the availability of independent verification for all relevant data. This ensures that the community members can independently verify the authenticity of the transactions and account verifications within the platform.
