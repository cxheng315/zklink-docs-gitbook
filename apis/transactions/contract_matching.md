Contract matching

| Name         | Type            | Mandatory | Description                                                                      |
|--------------|-----------------|-----------|----------------------------------------------------------------------------------|
| type         | String          | yes       | The value is "ContractMatching"                                                  |
| accountId    | AccountId       | yes       | The account id                                                                   |
| subAccountId | SubAccountId    | yes       | The subaccount id                                                                |
| maker        | Contract list   | yes       | The maker list                                                                   |
| taker        | [Contract]()    | yes       | The taker                                                                        |
| fee          | The fee         | yes       | The fee amount of ContractMatching                                               |
| feeToken     | TokenId         | yes       | The token id of the fee                                                          |
| signature    | ZkLinkSignature | yes       | the pub key hash corresponding to the signature must be aligned with the account |


where the `Contract` is the order in pertetual contract

| Name         | Type                                          | Description                                                                        |
|--------------|-----------------------------------------------|------------------------------------------------------------------------------------|
| accountId    | [AccountId](../data_types.md#AccountId)       | account id                                                                         |
| subAccountId | [SubAccountId](../data_types.md#SubAccountId) | sub account id                                                                     |
| slotId       | [SlotId](../data_types.md#SlotId)             | slot id                                                                            |
| nonce        | [Nonce](../data_types.md#Nonce)               | nonce                                                                              |
| pairId       | [PairId](../data_types.md#PairId)             | the pair id                                                                        |
| size         | BigUint                                       | position size                                                                      |
| price        | BigUint                                       | price                                                                              |
| direction    | u8                                            | 1: long, 0: short                                                                  |
| feeRates     | [u8, u8]                                      | The fee rates of [maker, taker]，100 means 1.00%                                    |
| hasSubsidy   | u8                                            | 1: true, 0: false, if the maker has subsidy, the submitter will give maker subsidy |
| signature    | [ZkLinkSignature](#ZkLinkSignature)           | ZkLink L2 signature                                                                |

For example:

```json
{
  "type": "ContractMatching",
  "accountId": 0,
  "subAccountId": 0,
  "maker": [
    {
      "accountId": 0,
      "subAccountId": 0,
      "slotId": 0,
      "nonce": 0,
      "pairId": 0,
      "size": "0",
      "price": "0",
      "direction": 0,
      "feeRates": [
        0,
        0
      ],
      "hasSubsidy": 0,
      "signature": {
        "pubKey": "0x99575738f142a942df9db99d27bd4ceeb8f4e75f9444b4cee4e3170965854404",
        "signature": "957826468392052073e13147ed3e8e1642dfea10cd423bbb9a795932a15a4c122fa5e71c35a7d59198fa2d7ed28bb1f44e5c5392049607347855243ddc027d00"
      }
    }
  ],
  "taker": {
    "accountId": 0,
    "subAccountId": 0,
    "slotId": 0,
    "nonce": 0,
    "pairId": 0,
    "size": "0",
    "price": "0",
    "direction": 0,
    "feeRates": [
      0,
      0
    ],
    "hasSubsidy": 0,
    "signature": {
      "pubKey": "0x43cbec0bf142a942df9db99d27bd4ceeb8f4e75f9444b4cee4e3170965854404",
      "signature": "366e759d61a5052073e13147ed3e8e1642dfea10cd423bbb9a795932a15a4c122fa5e71c35a7d59198fa2d7ed28bb1f44e5c5392049607347855243ddc027d00"
    }
  },
  "fee": "0",
  "feeToken": 0,
  "signature": {
    "pubKey": "0x1234567bf142a942df9db99d27bd4ceeb8f4e75f9444b4cee4e3170965854404",
    "signature": "1234567861a5052073e13147ed3e8e1642dfea10cd423bbb9a795932a15a4c122fa5e71c35a7d59198fa2d7ed28bb1f44e5c5392049607347855243ddc027d00"
  }
}
```

## sign contractMatching

{% tabs %}
{% tab title="Golang" %}
```go

```

For more detail please refer to [Golang example](https://github.com/zkLinkProtocol/zklink_sdk/tree/main/examples/Golang) in SDK
{% endtab %}

{%tab title="javascript" %}

```javascript

```

For more detail please refer to [javascript example](https://github.com/zkLinkProtocol/zklink_sdk/tree/main/examples/Javascript)
{% endtab %}
{% endtabs %}