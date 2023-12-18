## easy-mock-template-axios

基于 axios 的接口定义模板。

## Documentation

[帮助文档](https://easy-mock.github.io/easy-mock-cli/)

### 此模板扩展的配置

1. `projects.urlPreprocessor` type `function`, url 预处理, 在此你可以对你的每一个 api url 做调整
2. `projects.baseUrl` type `string`, default `"''"`

```javascript
// example
module.exports = {
  // easy-mock 服务器
  host: "http://easy-mock.gm",
  // 生成文件输入目录
  output: "src/api",
  // 生成代码使用的模板
  template: "gmsoft-happyCoding/axios-ts",
  projects: [
    {
      // easy-mock project id http://easy-mock.gm/project/5c514bf9cd2f550e9dfbb515
      id: "5c514bf9cd2f550e9dfbb515",
      name: "whatToEat",
      // urlPreprocessor: url => url.replace('/demo-gateway', ''),
      // 如果baseUrl为字符串请使用 "'baseUrl'"
      baseUrl: "process.env.REACT_APP_API_GATEWAY_BASE",
    },
    {
      // easy-mock project http://easy-mock.gm/project/5c7c941504e77820f451b643
      id: "5c7c941504e77820f451b643",
      name: "componentRegistry",
      baseUrl: "process.env.REACT_APP_COMPONENT_REGISTRY_SERVER",
    },
  ],
};
```
