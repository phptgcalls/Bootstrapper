# InputStorePaymentPurpose

**Description** : *Info about a Telegram Premium purchase*

**Layer** : 211

```tl
inputStorePaymentPremiumSubscription#a6751e66 flags:# restore:flags.0?true upgrade:flags.1?true = InputStorePaymentPurpose;
inputStorePaymentGiftPremium#616f7fe8 user_id:InputUser currency:string amount:long = InputStorePaymentPurpose;
inputStorePaymentPremiumGiftCode#fb790393 flags:# users:Vector<InputUser> boost_peer:flags.0?InputPeer currency:string amount:long message:flags.1?TextWithEntities = InputStorePaymentPurpose;
inputStorePaymentPremiumGiveaway#160544ca flags:# only_new_subscribers:flags.0?true winners_are_visible:flags.3?true boost_peer:InputPeer additional_peers:flags.1?Vector<InputPeer> countries_iso2:flags.2?Vector<string> prize_description:flags.4?string random_id:long until_date:int currency:string amount:long = InputStorePaymentPurpose;
inputStorePaymentStarsTopup#dddd0f56 stars:long currency:string amount:long = InputStorePaymentPurpose;
inputStorePaymentStarsGift#1d741ef7 user_id:InputUser stars:long currency:string amount:long = InputStorePaymentPurpose;
inputStorePaymentStarsGiveaway#751f08fa flags:# only_new_subscribers:flags.0?true winners_are_visible:flags.3?true stars:long boost_peer:InputPeer additional_peers:flags.1?Vector<InputPeer> countries_iso2:flags.2?Vector<string> prize_description:flags.4?string random_id:long until_date:int currency:string amount:long users:int = InputStorePaymentPurpose;
inputStorePaymentAuthCode#9bb2636d flags:# restore:flags.0?true phone_number:string phone_code_hash:string currency:string amount:long = InputStorePaymentPurpose;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**inputStorePaymentPremiumSubscription**](constructor/inputStorePaymentPremiumSubscription) | Info about a Telegram Premium purchase |
| [**inputStorePaymentGiftPremium**](constructor/inputStorePaymentGiftPremium) | Info about a gifted Telegram Premium purchase |
| [**inputStorePaymentPremiumGiftCode**](constructor/inputStorePaymentPremiumGiftCode) | Used to gift Telegram Premium subscriptions only to some specific subscribers of a channel/supergroup or to some of our contacts, see here » for more info on giveaways and gifts |
| [**inputStorePaymentPremiumGiveaway**](constructor/inputStorePaymentPremiumGiveaway) | Used to pay for a giveaway, see here » for more info |
| [**inputStorePaymentStarsTopup**](constructor/inputStorePaymentStarsTopup) | Used to top up the Telegram Stars balance of the current account |
| [**inputStorePaymentStarsGift**](constructor/inputStorePaymentStarsGift) | Used to gift Telegram Stars to a friend |
| [**inputStorePaymentStarsGiveaway**](constructor/inputStorePaymentStarsGiveaway) | Used to pay for a star giveaway, see here » for more info |
| [**inputStorePaymentAuthCode**](constructor/inputStorePaymentAuthCode) | NOTHING |