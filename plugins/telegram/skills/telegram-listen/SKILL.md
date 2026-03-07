---
name: telegram-listen
description: >
  启动 Telegram 消息监听循环。当用户说"监听 Telegram"、"开始 Telegram"、
  "listen telegram"、"启动 bot" 等时触发。
  进入 wait_for_message → 处理任务 → send_message 回复 → 继续等待 的循环。
---

# Telegram Listen — 消息监听循环

通过 Telegram Bot 接收用户消息，执行任务，回复结果。

## 流程

1. 调用 `mcp__telegram__wait_for_message` 阻塞等待新消息
2. 收到消息后，理解用户意图并执行对应任务
3. 调用 `mcp__telegram__send_message` 将结果回复到对应 `chat_id`
4. 回到步骤 1，继续等待下一条消息

## 规则

- 每次收到消息后，先完整执行任务，再回复结果
- 回复时使用消息中携带的 `chat_id`
- 如果任务执行失败，回复错误原因
- 如果消息内容不明确，回复询问用户意图
- 保持循环运行，直到用户在 Telegram 中发送"停止"或"stop"，或在终端中断
