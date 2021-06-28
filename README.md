# sublime HQ/sublime 4 typescript react 环境搭建(支持LSP)
现有submite HQ 默认集成了对typescript的支持，但是无验证typescript语法

## 安装sublime HQ，及插件
- Emmet(html snippet插件)
- JsPrettier(格式化代码)
- LSP (LSP服务提供支持)
- LSP-typescript(LSP typescript提供校验[https://github.com/sublimelsp/LSP-typescript])
- MarkdownEditing(MD文本编辑器)
- MarkdownHtmlPreview(MD文本预览)
- materialui-react-component-snippet-autocomplete(需要修改为支持typescript，此项目中会上传)
- Sublime ES7 React Redux ReactiveNative JS snippets(react相关snippet)

## 配置本地LSP服务
- Theia TypeScript Language Server(LSP校验服务[https://github.com/theia-ide/typescript-language-server])

## windows问题

### 执行`typescript-language-server --stdio`时报错
```sh
typescript-language-server : 无法加载文件 ...\node_global\typescript-language-server.ps1，因为在此系统上
禁止运行脚本。有关详细信息，请参阅 https:/go.microsoft.com/fwlink/?LinkID=135170 中的 about_Execution_Policies。
所在位置 行:1 字符: 1
+ typescript-language-server --stdio
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : SecurityError: (:) []，PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess
```

解决方法：
```sh
set-ExecutionPolicy RemoteSigned
#选Yes
```

## 使用
开发时需要提前启动LSP服务，启动命令
```sh
typescript-language-server --stdio
```
