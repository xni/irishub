# iriscli htlc claim

## 描述

将 HTLC 中锁定的资金发送到收款人地址

## 使用方式

```bash
iriscli htlc claim --hash-lock=<hash-lock> --secret=<secret>
```

## 标志

| 命令，速记    | 类型     | 是否必须 | 默认值 | 描述                          |
| ----------- | -------- | ------ | ----- | ---------------------------- |
| --hash-lock | bytesHex | 是     |       | 要发送锁定资金 HTLC 的 hash lock |
| --secret    | bytesHex | 是     |       | 用于生成 hash lock 的 secret    |

## 示例

### 将 HTLC 中锁定的资金发送到收款人地址

```bash
iriscli htlc claim \
--from=userX \
--hash-lock=f054e34abd9ccc3cab12a5b797b8e9c053507f279e7e53fb3f9f44d178c94b20 \
--secret=5f5f5f6162636465666768696a6b6c6d6e6f707172737475767778797a5f5f5f \
--fee=0.3iris \
--chain-id=testNet \
--commit
```