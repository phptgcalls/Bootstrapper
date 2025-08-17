# inputThemeSlug

**Description** : *Theme by theme ID*

**Layer** : 211

```tl
inputThemeSlug#f5890df1 slug:string = InputTheme;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>slug</mark> | [`string`](type/string) | Unique theme ID obtained from a theme deep link » |

---

## Type

[InputTheme](type/InputTheme)

---

## Example

```php
$inputTheme = $client->inputThemeSlug(
	slug : '2EjcUHIepwTZFJ5t',
);
```