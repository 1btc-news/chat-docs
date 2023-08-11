# Send Dust

After signing the message, the logged in account is registered with the [1btc Chat API](../1btc-chat-api.md#register-account), which uses the signature and public key to generate a unique Bitcoin address.

The generated Bitcoin address is _deterministic_, meaning if the same signature and public key are used, the same address is generated.

{% hint style="warning" %}
Nobody has access to the dust address, and the dust sent will not be returned.\
\
"Dust" is a tiny fraction of Bitcoin, commonly equal to 0.00006 BTC or 6,000 satoshis.
{% endhint %}

This proves access to the wallet with more than 1 BTC using the dust transaction, which the API actively monitors for in the background.

Upon successful receipt of the dust, the API verifies the user's account balance and marks it as verified.

### Dust Address Example

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
**This is an example, do not send funds to the address above.**
{% endhint %}
