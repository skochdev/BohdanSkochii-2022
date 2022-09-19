Create a `.prettierrc.json` file in the root of your project (outside _src/_, at one level with _package.json_)

Populate it with next settings:

```json
{

"singleQuote": true,

"tabWidth": 2,

"useTabs": false,

"bracketSameLine": true,

"bracketSpacing": true,

"semi": true,

"printWidth": 80,

"trailingComma": "es5",

"jsxBracketSameLine": false,

"arrowParens": "avoid",

"proseWrap": "always"

}
```

Prettier [docs](https://prettier.io/docs/en/index.html)