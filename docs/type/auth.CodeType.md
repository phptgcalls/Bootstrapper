# auth.CodeType

**Description** : *Type of verification code that will be sent next if you call the resendCode method*

**Layer** : 211

```tl
auth.codeTypeSms#72a3158c = auth.CodeType;
auth.codeTypeCall#741cd3e3 = auth.CodeType;
auth.codeTypeFlashCall#226ccefb = auth.CodeType;
auth.codeTypeMissedCall#d61ad6ee = auth.CodeType;
auth.codeTypeFragmentSms#6ed998c = auth.CodeType;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**auth.codeTypeSms**](constructor/auth.codeTypeSms) | The next time, the authentication code will be delivered via an immediately canceled incoming call |
| [**auth.codeTypeCall**](constructor/auth.codeTypeCall) | The next time, the authentication code is to be delivered via an outgoing phone call |
| [**auth.codeTypeFlashCall**](constructor/auth.codeTypeFlashCall) | The next time, the authentication code will be delivered via an immediately canceled incoming call |
| [**auth.codeTypeMissedCall**](constructor/auth.codeTypeMissedCall) | The next time, the authentication code will be delivered via an immediately canceled incoming call, handled manually by the user |
| [**auth.codeTypeFragmentSms**](constructor/auth.codeTypeFragmentSms) | The next time, the authentication code will be delivered via fragment.com |