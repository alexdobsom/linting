# ESlint, Prettier and Airbnb styleguide in VS Code

> Install the ESlint and Prettier extensions via the Extension UI

Hit <kbd>CTRL</kbd>+<kbd>,</kbd> -> format on save -> check

also:

<kbd>CTRL</kbd>+<kbd>,</kbd> -> Prettier -> enable/disable features like single or double quotes.

> Then:


```
npm init -y
```

```
npm eslint -g
```

```
npm i --dev eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node
```

``` 
npx install-peedeps --dev eslint-config-airbnb
or
eslint-airbnb-base [if no React project]
```
> now:

```
eslint --init  (if there is a eslint globally installed)
```
it's gonna generate a **.eslint.config** file, but want matters is:
```
{
  extends: ["airbnb", "prettier", "plugins:node/recommended"],
  plugins: ["prettier"],
  rules: {
    "prettier/prettier": "warn" [to see prettier errors]
    "no-unused-vars": "warn",
    "no-console": "off",
    "func-names": "off",
    "class-methods-use-this": "warn",
    "no-process-exit": "off", [for node]
    //add more rules here (from website documentation)
  }
}
```

Create a **.prettierrc** file to make more configuration like:
```
{
  singlequote: true
}
```

see more here: https://www.youtube.com/watch?v=SydnKbGc7W8