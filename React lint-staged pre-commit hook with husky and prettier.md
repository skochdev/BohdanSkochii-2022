This setup will analyze your commits and attempt to fix your code in case it's styling is messed up, throws an error if it fails, so you won't commit defectively styled code to git

1. Install dependencies :

`npm install --save-dev prettier eslint`

2.Initialize the **lint-staged** and **husky**:

`npx mrm lint-staged`

[[prettierrc.json config for Prettier]]

