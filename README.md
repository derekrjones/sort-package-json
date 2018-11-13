## Sort Package.json

fork of [sort-package-json](https://github.com/keithamus/sort-package-json)

tailored to my own personal preference, since `sort-package-json` is opinionated and (intentionally) doesn't support config

### Install

note: this is not published to npm

```bash
git clone git@github.com:derekrjones/sort-package-json.git
cd sort-package-json
npm i
npm link
```

### Usage

```bash
cd path/to/some/repo
sort-package-json       # sorts ./package.json
sort-package-json packages/*/package.json example/package.json
```

### Differences

#### group entry points

`bin`, `main`, `module`, `browser`

#### 3rd party fields below common fields

- bad: `eslintIgnore`, `jest`, `dependencies`, `devDependencies`
- good: `dependencies`, `devDependencies`, `eslintIgnore`, `jest`

#### Keep keyword order

- bad: `a b MyNamespace y z`
- good: `MyNamespace a b y z`
