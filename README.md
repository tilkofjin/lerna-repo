## [Lerna](https://github.com/lerna/lerna) & [Yarn Workspace](https://classic.yarnpkg.com/blog/2017/08/02/introducing-workspaces/)

```bash
# 安装依赖
yarn

# 启动子应用示例
yarn vue:dev


# 所有子应用统一安装包，例如安装 redux
lerna add redux

# 移除所有子应用依赖的公共包，例如移除所有子应用的 redux
lerna exec -- yarn remove redux

# 安装本地包依赖，执行完后 taro3 会增加新的 dependencies，然后就可以在 taro3 中使用 pubcomp:
lerna add pubcomp --scope=taro3

# 将 taro3 中的 pubcomp 依赖移除
lerna exec --scope=taro3  yarn remove pubcomp
```

实用教程：
  - [lerna 和 yarn 实现 monorepo](https://juejin.cn/post/6855129007185362952#heading-14)
  - [lerna多包管理实践](https://juejin.cn/post/6844904194999058440)