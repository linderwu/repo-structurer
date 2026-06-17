---
type: index
title: patterns — Runtime Experience
description: 系統上線後才浮現的反覆模式。包含 known issues、debug 線索、效能觀察、workaround 背景故事。來源是 runtime，不是 design-time。
tags: [patterns, runtime, debug, known-issues, performance, troubleshooting]
---

# patterns/ — Runtime Experience

## 這是什麼

patterns/ 是 runtime-learned knowledge 層。跟 `wiki/concepts/` 的區別：

- **wiki/concepts/** — 回答「這個系統是什麼」（design-time 的靜態描述）
- **patterns/** — 回答「路上踩過什麼坑、怎麼修」（runtime 的教訓）

## 內容類型

### Known Issues
系統在特定條件下會爆的問題。不是 bug，是已知限制。

### Debug 線索
「500 錯誤先查 connection pool，別浪費時間查 JWT」這類經驗。

### 效能觀察
「日活超過 5000 時，這條 query 會慢四倍」這類 profiling 結論。

### Workaround 背景故事
「不是架構決策，是某天半夜緊急上的 hotfix，後來發現有更好的做法但來不及改」。

### Incident Post-Mortem 結論
不是 timeline，是學到的東西。每一個 incident 結案後都應該在這裡留下一筆。

## 格式

```markdown
---
type: pattern
title: [問題或主題]
date: YYYY-MM-DD
tags: [relevant, tags]
---

# [問題或主題]

## 背景
什麼情況下發現的。

## 問題
當時的癥狀或錯誤。

## 根因
（如果知道）為什麼會這樣。

## 解法
當時怎麼修的。

## 預防
未來怎麼避免再踩同樣的坑。

## 相關
- [[../decisions/xxx]] — 相關的設計決策
- [[../concepts/yyy]] — 相關的概念
```

## 歸檔時機

- 踩坑後
- On-call 後
- Incident post-mortem 後
- 任何「這個知識是上線後才發現的」時刻

## 與 decisions/ 的區別

| | patterns/ | decisions/ |
|--|-----------|------------|
| **焦點** | 問題 → 解法 | 選項 → 理由 |
| **來源** | Runtime 觀察 | Design-time 決策 |
| **時機** | 上線後才會有 | 設計時就會有 |
| **例子** | timeout 300s 不夠，改成 500s | 選 REST 而非 gRPC |

## 現有頁面

（空，等待歸檔）
