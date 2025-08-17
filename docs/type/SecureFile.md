# SecureFile

**Description** : *Secure passport file, for more info see the passport docs »*

**Layer** : 211

```tl
secureFileEmpty#64199744 = SecureFile;
secureFile#7d09c27e id:long access_hash:long size:long dc_id:int date:int file_hash:bytes secret:bytes = SecureFile;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**secureFileEmpty**](constructor/secureFileEmpty) | Empty constructor |
| [**secureFile**](constructor/secureFile) | Secure passport file, for more info see the passport docs » |