# EpayLDC - LINUX DO Credit 积分支付插件

适用于 [Xboard](https://github.com/cedar2025/Xboard) 的 LINUX DO Credit 积分支付插件。

## 特性

- ✅ 兼容 LINUX DO Credit 易支付接口
- ✅ 通过主动查询确认支付状态（不依赖异步通知回调）
- ✅ 每分钟自动检查待支付订单
- ✅ 与 Xboard 自带的 Epay 插件完全隔离

## 安装

1. 下载本仓库 ZIP 或 Clone
2. 将 `EpayLDC` 文件夹放入 Xboard 的 `plugins/` 目录
3. 在 Xboard 后台 -> 插件管理 中启用插件

## 配置

### Xboard 后台

| 配置项 | 说明 | 示例 |
|-------|-----|------|
| 支付网关地址 | LDC 网关 | `https://credit.linux.do/epay` |
| 商户ID | pid | 从 LDC 后台获取 |
| 通信密钥 | key | 从 LDC 后台获取 |
| 支付类型 | 固定 | `epay` |

### LINUX DO Credit 后台

| 配置项 | 建议填写 |
|-------|---------|
| notify_url | `https://你的域名/` |
| return_url | `https://你的域名/` |

## 注意事项

- 支付确认最大延迟约 1 分钟（定时任务轮询）
- 确保 Xboard 定时任务正常运行

## License

MIT
