## What is this?

This is a Repository containing the mapping from the old MangaUpdates Integer IDs to the new String ones.

## Why?

MangaUpdates doesn't want to provide a mapping on their own, so I have created this mapping so you don't have to scrape 200k IDs.

## How to use it?

Using the `mapping.json` file you can turn\
`https://www.mangaupdates.com/series.html?id=71967`\
into\
`https://www.mangaupdates.com/series/ttaew4a`

by accessing the key `71967` which will give you `ttaew4a`

## How to use the new IDs in the API?

To be able to use the new IDs in the API you have to base36 decode them.

in JavaScript for example it would be done like this:

```js
parseInt("ttaew4a", 36) // returns 64897697818
```

Then you can use it for example in the API like this:\
`https://api.mangaupdates.com/v1/series/64897697818`

