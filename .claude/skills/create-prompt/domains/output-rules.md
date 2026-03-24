# 出力規則（プロンプト合成の最上位ルール）

## メタデータ
- priority: 10
- conflicts: []

## ルール

### 対象エンジン
- nijijourney v7 / midjourney v7

### 基本姿勢
- プロンプトを雰囲気や文脈ではなく、語義・構造・視覚定義の粒度で比較的忠実に解釈する前提で扱う
- 曖昧な雰囲気語・慣用的ジャンル語・省略ラベルには依存しない
- 形・比率・線の役割・色層・質感・情報密度といった視覚的に解釈可能な要素へ必ず分解して記述する
- 常に「規制されにくい」「破綻しにくい」「再現性の高い」プロンプト生成を行う

### 優先順位（絶対）
1. 画風成立
2. 主役の視認性
3. 配色成立
4. 構造維持
5. 情報再現

- 入力情報よりも、画面としての成立を常に優先する

### 思想の核
- 余白（密度差）
- 色相による成立
- 影色に別色相混合
- 視線誘導
- 主題は一つ

### 概念語・ジャンル語の扱い（最重要）
概念語は単体では使用しない。使用する場合：
```
[concept term], defined as [visual description]
または
[concept term], visually interpreted as [visual description]
```
概念語は補助であり、主役は必ず visual description 側とする。

### プロンプト出力形式
- プロンプトは英語で出力（主）
- 各文はカンマ区切りのフレーズ列
- 1フレーズ＝1視覚的意図
- 意味衝突・過剰形容を避ける
- 英語プロンプトの後に日本語訳を併記
- 主題語を直接書かない

### プロンプト優先順（固定）
1. 主役物理定義
2. 焦点物体
3. 髪
4. 目
5. 肌
6. 衣装層
7. ポーズ＋カメラ位置
8. 光
9. 画材
10. 技法
11. 色面構造
12. 影色混合
13. 背景
14. 密度差
15. 線の役割
16. 禁止要素

### 禁止ブロック（統合プロンプト末尾に必ず付与）
- no photorealism
- no heavy outlines
- no pure black lines
- no uniform digital shading

### 補助要素の扱い
- 新キャラクターは追加しない
- 物語的設定は追加しない
- ただし空間成立・奥行き成立に必要な最小限の色面・物体は追加可能
- 補助要素は主役より目立たせない

### 空間の明示
- 具体的な空間タイプを必ず一つ指定する
- 時間帯または光条件を必ず一つ指定する
- 空間は色面と奥行きとして成立させる

### 表現全体の前提
- 写真、写実、フォトリアルな描写は明確に避ける
- すべての出力は「最初から描かれたイラスト」として成立させる
- 写真由来の質感、均一で滑らかな表面、過度に完成されたデジタル処理は使用しない

### メモリ・慣性対策
新規生成時は以下を適用：
- 完全新規仕様として扱う
- 過去の色相・光・画材を参照しない
- 以前使用した語彙・支配色を再利用しない
- 同一髪色・素材・光条件が出た場合は変更
- 内部で必ず変更する項目：支配色相系統、素材カテゴリ、光の種類、画材カテゴリ

### 最終確認チェックリスト
- 主役は、線やにじみ、装飾に埋もれていないか
- 雰囲気は良いが、何の絵か分からない状態になっていないか
- 技法や表現が前面に出すぎていないか

## キーワード
- 使用禁止: photo, realistic, photorealistic, hyper-realistic, 3D render, digital art（単体）
- 推奨: illustration, painted, drawn, depicted
- 必須末尾: no photorealism, no heavy outlines, no pure black lines, no uniform digital shading

## 例
（ドメイン単体での出力例はなし。合成時の最上位判断基準として機能する）

### 主語先頭安定テンプレ
```
[physical subject definition],
[focal object or material],
[hair description],
[eye description],
[skin description],
[layered clothing structure],
[pose + camera position],
[lighting definition],
[painting medium visually interpreted as …],
[technique defined as …],
[color-plane structure],
[shadow mixed with secondary hue],
[background space type],
[density contrast],
[line role clarification],
[color harmony block],
[prohibition block]
```
