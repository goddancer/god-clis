### 安装依赖

`npm install`

### 启动

`npm run watch`

### 执行 `npm link`

* 在未link `god-clis` command之前，需要先去掉钩子`"postinstall": "god-clis config set"`，否则会一直报错而无法成功安装

* `postinstall`是npm安装过程中的一个生命周期钩子，`package.json`中定义了，会自动执行

此时就可以使用 `god-clis` 命令了。

`god-clis` commands:

- `god-clis init babel-template myNpm`
- `god-clis config get`
- `god-clis config set type orgs`
- `god-clis config set registry babel-template`

- `god-clis config set type users`
- `god-clis config set registry goddancer`

### publish

* 执行`npm publish`之后，可以在24h内，执行`npm unpublish -f | npm unpublish god-clis@1.x.x`进行撤回

* 需要注意的是，撤回以后的版本，需要24h以后才可以再次发布