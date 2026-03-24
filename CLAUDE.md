# create-prompt-niji7

niji journey用プロンプト生成プロジェクト。

## 概要
入力情報からniji journey v7向けの画像生成プロンプト（英語/日本語）を生成する。
ドメインカプセル（世界観・画風・色彩・顔構造 等）を合成してプロンプトを構築する。

## ディレクトリ構造
```
.
├── CLAUDE.md                          # プロジェクトルール
├── .devcontainer/                     # devcontainer設定
├── .claude/
│   ├── settings.json
│   └── skills/
│       └── create-prompt/
│           ├── SKILL.md               # プロンプト生成スキル本体
│           └── domains/               # ドメインカプセル（9種）
│               ├── _template.md       # カプセルテンプレート
│               ├── output-rules.md    # [10] 合成最上位ルール
│               ├── face-expression.md # [9]  顔・表情・目元
│               ├── art-style.md       # [8]  画風・線質・色面構造
│               ├── character-form.md  # [8]  造形・絵柄ポジション
│               ├── coloring.md        # [7]  色彩・配色・影色
│               ├── painterly-texture.md # [7] 絵画的質感・画材
│               ├── composition.md     # [5]  情報密度・視線誘導
│               ├── character.md       # [4]  キャラ外観基礎
│               └── world-setting.md   # [3]  世界観・環境
├── prompts/
│   ├── history/                       # プロンプト履歴（会話ログ兼ワークシート）
│   │   ├── _template.md              # 履歴テンプレート
│   │   └── YYYY-MM-DD_HHmm_{title}.md
│   └── input.md                       # 作業用メモ
└── .gitignore
```

## ワークフロー
1. `/create-prompt {描きたいもの}` を実行
2. 履歴ファイルが `prompts/history/` に自動作成される
3. 英語/日本語プロンプトが画面表示＋履歴ファイルに記録（v1）
4. 「修正して」「もっと研ぎ澄ましたい」→ 修正版がv2, v3...と追記される
5. 修正指示もそのまま履歴に記録される
6. 既存の履歴ファイルを渡して再開も可能

## ルール
- プロンプト生成時は必ずドメインカプセルを参照し、カプセル間の指示が矛盾しないよう合成する
- 履歴ファイルは上書きしない（追記のみ）
- ドメインカプセルの追加・編集はユーザーが行う
- 1つの履歴ファイル = 1つのプロンプト作品の全会話ログ
