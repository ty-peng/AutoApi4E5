# AutoApi4E5

## About

- 为什么要自己新建一个项目？  
  ~~他们的代码实在看不下去了（小声哔哔）~~  
  增强自己的动手实践能力

- 原理  
  利用 GitHub Actions 提供的免费容器定时调用 E5 订阅相关的 API，以保持作为开发者的活跃，然后看微软心情给不给你续期。

## How to use

此处仅介绍关键部分步骤，其他请参考下方原博文链接

### 配置

- `refresh_token.txt` 中填写你获取的 refresh_token
- 进入 GitHub 仓库设置 `Settings > Serets`
- 添加 `APP_ID`，填写你的 Azure 应用 ID
- 添加 `APP_SECRET`，填写你的 Azure 应用密钥
- 添加 `GH_TOKEN`，填写你的 GitHub 个人令牌

### 触发

- 立即触发

  点击项目右上角的 `☆ Star` 立即触发第一次 GitHub Action 工作流

- 定时调度

  目前定时调度设置的是 `12 */6 * * *` 每 6 个小时的第 12 分自动触发，可以在 `.github\workflows\autoapi.yml` 自行修改

## Notice

- 由于目前没有官方说明续期条件，所以，不保证一定能续期
- 不明白的地方先看下方参考链接

## Reference

- [参考原教程博文](https://blog.432100.xyz/index.php/archives/50/)
- [参考 GitHub Action 配置](https://github.com/wangziyingwen/AutoApiSecret))
