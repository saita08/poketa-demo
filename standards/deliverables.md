# 成果物管理規定

Poketaにおける成果物の保存・命名・フォーマットのルール。

## 保存場所

| 成果物 | 保存先 | 例 |
|--------|--------|-----|
| 議事録 | `docs/` | `docs/meeting-001.md` |
| 企画書 | `projects/{タイトル名}/` | `projects/ohanabatake/design.md` |
| 技術設計書 | `projects/{タイトル名}/` | `projects/ohanabatake/tech-spec.md` |
| アセット仕様 | `projects/{タイトル名}/` | `projects/ohanabatake/assets.md` |
| 参考資料 | `references/` | `references/colormixing-research.md` |
| 社内規定 | `standards/` | `standards/meeting-rules.md` |

## 命名規則

### 議事録
- 形式: `meeting-{連番3桁}.md`
- 例: `meeting-001.md`, `meeting-002.md`
- 連番は会議の開催順に振る

### プロジェクト成果物
- プロジェクトフォルダ名は英語の小文字ケバブケース
- 例: `projects/ohanabatake/`, `projects/juice-maker/`
- ファイル名は内容を端的に表す英語名
- 例: `design.md`(企画書), `tech-spec.md`(技術設計), `assets.md`(アセット仕様)

### 社内規定
- 内容を端的に表す英語のケバブケース
- 例: `meeting-rules.md`, `hiring-policy.md`, `deliverables.md`

## フォーマット

- 全ての文書はMarkdown形式(.md)で記述する
- 日本語で記述する。技術用語やコード識別子は原語のまま
- 文書の先頭には見出し(h1)でタイトルを記載する
- 議事録には日時・参加者・議題を必ず含める

### 議事録の構成

議事録は「結論」と「過程」を明確に分離する。忙しいときは冒頭だけ読めば状況がわかるようにする。

```
# 第N回会議 議事録

- 日時 / 参加者 / 議題

## 結論
- 最終合意事項
- 決定したスコープ(IN/OUT)
- 次のアクション

## 未決事項
- 持ち越しになった論点(あれば)

## 議論の過程
### ラウンドN: (目的)
- 各社員の主張の要約
- 社員間の直接議論で出た論点
- そのラウンドでの収束点
```

## 版管理

- 成果物の更新はgitで管理する
- 大きな変更にはコミットメッセージで変更理由を残す
- 過去の版を参照したい場合はgit logで辿る(ファイル名にバージョン番号をつけない)
