# apple-tv-build

使用 GitHub macOS runner 构建 OrionTV 的 Apple TV 真机安装包，无需本地 Mac。

- 上游：[orion-lib/OrionTV](https://github.com/orion-lib/OrionTV)，版本 1.3.14。
- 固定源码提交：`41c7a6005985e5543b9bf302cdd4233d82f1ead5`。
- 运行方式：进入 **Actions → Build OrionTV for Apple TV (experimental) → Run workflow**。
- 成功后在该次运行的 **Artifacts** 下载 `OrionTV-tvos-unsigned`（保留 7 天）。
- 下载内容包括未签名 IPA 和 SHA256 校验文件，必须通过支持 tvOS 的工具签名后才能安装。
- 可在同一局域网的 Linux NAS 上使用 [ATVLoadly](https://github.com/bitxeno/atvloadly) 配对、签名及安装。
- 电视客户端需要连接兼容的 MoonTV／LunaTV 后端，并配置自己的数据源。

此仓库和 GitHub 构建过程不需要 Apple ID、NAS 密码或签名私钥。请勿将这些信息提交到仓库。

构建成功只说明能生成安装包；实际启动、遥控器操作、登录和播放仍需在 Apple TV 上验证。
