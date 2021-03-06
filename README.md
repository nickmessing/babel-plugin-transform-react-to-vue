# babel-plugin-transform-react-to-vue

[![NPM version](https://img.shields.io/npm/v/babel-plugin-transform-react-to-vue.svg?style=flat)](https://npmjs.com/package/babel-plugin-transform-react-to-vue) [![NPM downloads](https://img.shields.io/npm/dm/babel-plugin-transform-react-to-vue.svg?style=flat)](https://npmjs.com/package/babel-plugin-transform-react-to-vue) [![CircleCI](https://circleci.com/gh/vueact/babel-plugin-transform-react-to-vue/tree/master.svg?style=shield)](https://circleci.com/gh/vueact/babel-plugin-transform-react-to-vue/tree/master)  [![donate](https://img.shields.io/badge/$-donate-ff69b4.svg?maxAge=2592000&style=flat)](https://github.com/egoist/donate)

🚧 **In development...**

## Install

```bash
yarn add babel-plugin-transform-react-to-vue --dev
```

## Usage

```js
{
  "plugins": ["transform-react-to-vue"]
}
```

Input:

```js
class Counter extends Component {
  state = { count: 0 }

  inc = () => this.setState({count: this.state.count + 1})

  render() {
    return <button onClick={this.inc}>
      {this.state.count}
    </button>
  }
}
```

Output:

```js
var Counter = {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    inc() {
      this.count = this.count + 1
    }
  },
  render() {
    return <button onClick={this.inc}>
      {this.count}
    </button>
  }
}
```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D


## Author

**babel-plugin-transform-react-to-vue** © [egoist](https://github.com/egoist), Released under the [MIT](./LICENSE) License.<br>
Authored and maintained by egoist with help from contributors ([list](https://github.com/vueact/babel-plugin-transform-react-to-vue/contributors)).

> [egoistian.com](https://egoistian.com) · GitHub [@egoist](https://github.com/egoist) · Twitter [@_egoistlily](https://twitter.com/_egoistlily)
