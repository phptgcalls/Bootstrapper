# SecurePasswordKdfAlgo

**Description** : *KDF algorithm to use for computing telegram passport hash*

**Layer** : 211

```tl
securePasswordKdfAlgoUnknown#4a8537 = SecurePasswordKdfAlgo;
securePasswordKdfAlgoPBKDF2HMACSHA512iter100000#bbf2dda0 salt:bytes = SecurePasswordKdfAlgo;
securePasswordKdfAlgoSHA512#86471d92 salt:bytes = SecurePasswordKdfAlgo;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**securePasswordKdfAlgoUnknown**](constructor/securePasswordKdfAlgoUnknown) | Unknown KDF algo (most likely the client has to be updated) |
| [**securePasswordKdfAlgoPBKDF2HMACSHA512iter100000**](constructor/securePasswordKdfAlgoPBKDF2HMACSHA512iter100000) | PBKDF2 with SHA512 and 100000 iterations KDF algo |
| [**securePasswordKdfAlgoSHA512**](constructor/securePasswordKdfAlgoSHA512) | SHA512 KDF algo |