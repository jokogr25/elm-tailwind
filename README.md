# Installing
Following this guide [https://dev.to/codewithcats/set-up-elm-project-with-tailwindcss-parcel-14gc](https://dev.to/codewithcats/set-up-elm-project-with-tailwindcss-parcel-14gc) did not work entirely.

Installing parcel in a version >= v2, tailwindcss >= v4, postcss >= v4 did the trick:
```shell
npm install tailwindcss @tailwindcss/postcss postcss parcel
```

Instead of `postcss.config.js` following file needed to be created:
`.postcssrc.json`
```json
{
    "plugins": {
        "@tailwindcss/postcss": {}
    }
}
```

The content of `tailwind.css`:
```css
@import "tailwindcss";
```
