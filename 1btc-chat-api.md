# 1BTC Chat API

{% swagger method="get" path="" baseUrl="https://1btc-api.console.xyz/" summary="System Info" %}
{% swagger-description %}
Returns network information and minimum valid BTC balance.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
```typescript
{
    network: string, // "testnet" | "mainnet"
    minValid: string // big number with 8 decimals
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="" baseUrl="https://1btc-api.console.xyz/account/:address" summary="Account Info" %}
{% swagger-description %}
Returns the owner address, randomly generated receive address, origin, and status.
{% endswagger-description %}

{% swagger-parameter in="path" name="address" required="true" %}
wallet address to check
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```typescript
{
    owner: string,                      // owner hiro wallet address (maybe evm, solana... in the future)
    receiveAddress: string,             // randomly generated bitcoin adress to deposit dust amount
    origin: string | undefined | null,  // the detected bitcoin address sent dust amount to receiveAddress
    status: string                      // "pending" | "valid" | "invalid"
                                        // pending  => waiting for the dust amount
                                        // valid    => origin balance gte minValid
                                        // invalid  => origin balance lt minValid
}
```
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="" %}
```typescript
{
    error: string
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="" baseUrl="https://1btc-api.console.xyz/get-hiro-signature-message" summary="Request Message" %}
{% swagger-description %}
Generates a new signature message for a wallet address.
{% endswagger-description %}

{% swagger-parameter in="body" name="wallet" required="true" %}
wallet address
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```typescript
{
    msg: string // message to use for signature request from the user
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```typescript
{
    error: string
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="" baseUrl="https://1btc-api.console.xyz/register-hiro" summary="Register Account" %}
{% swagger-description %}
Registers new account using Hiro wallet signature and public key.
{% endswagger-description %}

{% swagger-parameter in="body" name="signature" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="publicKey" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```typescript
{
    owner: string,                      // owner hiro wallet address (maybe evm, solana... in the future)
    receiveAddress: string,             // randomly generated bitcoin adress to deposit dust amount
    origin: string | undefined | null,  // the detected bitcoin address sent dust amount to receiveAddress
    status: string                      // "pending" | "valid" | "insufficient"
                                        // pending  => waiting for the dust amount
                                        // valid    => origin balance gte minValid
                                        // invalid  => origin balance lt minValid
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```typescript
{
    error: string
}
```
{% endswagger-response %}
{% endswagger %}
