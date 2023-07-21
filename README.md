# 1btc Chat

## Introduction

**1btc Chat is a unique community designed specifically for Bitcoin holders who possess at least 1 BTC.**

This platform aims to bring together this exclusive group, leveraging their strong value signal and enabling them to collaborate and shape their own narrative.

## Comparison with other platforms

The 1btc Chat platform sets itself apart from other social platforms like Discord and Telegram, which typically employ traditional authentication methods.

Instead, 1btc Chat adopts a wallet-first approach, where users' cryptocurrency address serves as their identity within the chat. This approach allows for pseudonymity while prioritizing privacy and security.

## Verifying a 1btc Holder

To ensure the authenticity of the community, it is crucial to verify that a user possesses at least 1 BTC. This verification process involves the following steps:

1. **Connect a Wallet:** Connect with either a Hiro or Xverse wallet, both renowned leaders in Bitcoin standards on the web. This is used to to generate the required signatures and determine the dust address for verification.
2. **Sign a Message:** Sign a message from the API to prove ownership of the logged in wallet, which in turn will generate a unique BTC address for verification.
3. **Send Dust Transaction:** Send a minimal amount of Bitcoin from the address with more than 1 BTC to the generated BTC address. This amount is commonly referred to as "dust" and equal to 0.00006 BTC or 6,000 satoshis.\
   <mark style="color:orange;">**Note: nobody has access to this address, and the dust will not be returned.**</mark>
4. **Await Verification:** The API actively monitors the generated BTC address for receiving the dust transaction. Upon successful receipt of the dust, the API verifies the user's account balance and marks it as verified.\
   <mark style="color:orange;">**Note: if the user spends any Bitcoin from the address, their verified status will be revoked, resulting in the loss of access to the chat.**</mark>

## Security and Privacy

1btc Chat places the utmost importance on security measures. The utilization of a dust transaction ensures that the user's funds remain securely stored in their primary wallet. Furthermore, the adoption of a separate wallet for the login account minimizes the risk of compromising the user's funds. Users are strongly advised to review and verify all transactions to ensure their security.

Nevertheless, it is essential to acknowledge privacy concerns. Bitcoin transactions are inherently traceable, which can potentially compromise user identities. To address these concerns, users can consider transferring their Bitcoin to and from exchanges or implementing privacy-enhancing techniques such as CoinJoin.

## Independent Verification and API Usage

The transparency and integrity of the 1btc Chat community are further reinforced through the availability of independent verification for all relevant data. This ensures that the community members can independently verify the authenticity of the transactions and account verifications within the platform.
