# SecureValue

**Description** : *Secure Telegram Passport value*

**Layer** : 211

```tl
secureValue#187fa0ca flags:# type:SecureValueType data:flags.0?SecureData front_side:flags.1?SecureFile reverse_side:flags.2?SecureFile selfie:flags.3?SecureFile translation:flags.6?Vector<SecureFile> files:flags.4?Vector<SecureFile> plain_data:flags.5?SecurePlainData hash:bytes = SecureValue;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**secureValue**](constructor/secureValue) | Secure value |