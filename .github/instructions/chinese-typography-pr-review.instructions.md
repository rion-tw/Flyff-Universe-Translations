---
name: chinese-typography-pr-review
description: "Use when: reviewing PRs for Simplified_Chinese or Traditional_Chinese translations. Apply Chinese typography and spacing rules for consistency and proper font rendering."
applyTo: 
  - "Simplified_Chinese/**"
  - "Traditional_Chinese/**"
---

# 中文翻譯 PR Review 規則

## 概述
此規則適用於檢查 Simplified_Chinese 或 Traditional_Chinese 資料夾中的翻譯 PR，確保翻譯內容符合排版和字型規範。

## 審查規則

### 1. 禁止使用全型標點符號
翻譯結果**不能包含**以下全型符號，必須改用對應的半形符號。全型符號會因現有字型而導致排版跑版。

| 禁用（全型） | 改用（半形） | 說明 |
|------------|-----------|------|
| `（` | `(` | 左括號 |
| `）` | `)` | 右括號 |
| `：` | `:` | 冒號 |

**範例**：
- ❌ `角色技能（高級説明）` → ✅ `角色技能(高級説明)`
- ❌ `提示：請注意` → ✅ `提示: 請注意`

### 2. 括號前後的空白規則

#### 規則 2a：左括號前
若 `(` 前面有**非標點符號**（如中文字、英文字母、數字），應在括號前補一個空白。

**範例**：
- ❌ `物品(Sword)` → ✅ `物品 (Sword)`
- ❌ `技能(Level 5)` → ✅ `技能 (Level 5)`
- ✅ `(開始)` → 保持不變（前面無其他字元）
- ✅ `等級 (Level)` → 保持不變（已有空白）

#### 規則 2b：右括號後
若 `)` 後面有**非標點符號**（如中文字、英文字母、數字），應在括號後補一個空白。

**範例**：
- ❌ `)字元` → ✅ `) 字元`
- ❌ `)但` → ✅ `) 但`
- ✅ `)。` → 保持不變（後面是標點符號）
- ✅ `) 字元` → 保持不變（已有空白）

### 3. 標點符號例外
括號前後已有標點符號時，無需額外補空白：
- `(Level).` → 保持不變
- `,Level)` → 保持不變

## 審查檢查清單

- [ ] 檢查是否有全型的 `（`、`：`、`）`
- [ ] 檢查 `(` 前是否需要補空白（前面有非標點符號時）
- [ ] 檢查 `)` 後是否需要補空白（後面有非標點符號時）
- [ ] 確認修正後的文本是否讀起來自然

## 範例檔案檢查

如果 PR 修改了 `Simplified_Chinese/Skills.csv` 或 `Traditional_Chinese/Dialogs.csv` 等檔案，請按照上述規則逐行檢查。

---

**最後更新**：2026年4月11日
