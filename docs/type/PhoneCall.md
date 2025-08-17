# PhoneCall

**Description** : *Phone call*

**Layer** : 211

```tl
phoneCallEmpty#5366c915 id:long = PhoneCall;
phoneCallWaiting#c5226f17 flags:# video:flags.6?true id:long access_hash:long date:int admin_id:long participant_id:long protocol:PhoneCallProtocol receive_date:flags.0?int = PhoneCall;
phoneCallRequested#14b0ed0c flags:# video:flags.6?true id:long access_hash:long date:int admin_id:long participant_id:long g_a_hash:bytes protocol:PhoneCallProtocol = PhoneCall;
phoneCallAccepted#3660c311 flags:# video:flags.6?true id:long access_hash:long date:int admin_id:long participant_id:long g_b:bytes protocol:PhoneCallProtocol = PhoneCall;
phoneCall#30535af5 flags:# p2p_allowed:flags.5?true video:flags.6?true conference_supported:flags.8?true id:long access_hash:long date:int admin_id:long participant_id:long g_a_or_b:bytes key_fingerprint:long protocol:PhoneCallProtocol connections:Vector<PhoneConnection> start_date:int custom_parameters:flags.7?DataJSON = PhoneCall;
phoneCallDiscarded#50ca4de1 flags:# need_rating:flags.2?true need_debug:flags.3?true video:flags.6?true id:long reason:flags.0?PhoneCallDiscardReason duration:flags.1?int = PhoneCall;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**phoneCallEmpty**](constructor/phoneCallEmpty) | Empty constructor |
| [**phoneCallWaiting**](constructor/phoneCallWaiting) | Incoming phone call |
| [**phoneCallRequested**](constructor/phoneCallRequested) | Requested phone call |
| [**phoneCallAccepted**](constructor/phoneCallAccepted) | An accepted phone call |
| [**phoneCall**](constructor/phoneCall) | Phone call |
| [**phoneCallDiscarded**](constructor/phoneCallDiscarded) | Indicates a discarded phone call |