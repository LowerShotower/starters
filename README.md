On .huskyrc.json file:
```
{
"hooks": {
"pre-commit": "lint-staged",
"pre-push": "npm run test:noWatch"
}
}
```
On ‘package.json’:
```
...
"scripts": {
...
"test": "react-scripts test",
"test:noWatch":"npm run test -- --watchAll=false",
"lint": “eslint --fix"
...
},
...
```

On ‘.lintstagedrc.json’:
```
{
"src/**/*.{js,ts,jsx,tsx}": [
"npm run lint"
]
}
```