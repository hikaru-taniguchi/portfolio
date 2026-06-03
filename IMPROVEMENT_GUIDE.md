
# 📋 ポートフォリオ改善ガイド
## hikaru-taniguchi用 実行マニュアル

---

## ✨ このドキュメントについて

このマニュアルは、あなたのリポジトリをもっと採用担当者に評価されるようにするための
**具体的な変更方法**を書いています。

📌 **各セクション**：
- **今の状態**: 現在どうなっているか
- **問題点**: なぜダメなのか
- **改善方法**: 具体的に何をするか
- **手順**: ステップバイステップ

---

---

# 改善プロジェクト1️⃣

## 🌤️ weather-todo-app（お天気 + ToDo）

### 📌 今の状態
```
✅ 機能は完成している
✅ デモサイトもある
✅ ライセンスも記載

❌ README が短すぎる
❌ 「何を学んだのか」が書いていない
❌ 完成度の表示がない
```

### 🔴 問題点
- 採用担当者が見ても「何がすごいのか」わからない
- 「このひと、どのレベルの開発者なの？」が伝わらない

---

### ✅ 改善方法

#### 📝 やることリスト
```
[ ] 1. README.md を新しく書く
[ ] 2. Status Badge（完成度表示）を追加
[ ] 3. .gitignore を確認・追加
[ ] 4. GitHub Topics を設定
```

---

### 🔧 手順1: README.md を改善

#### **現在の README**
```markdown
# 🌤️ お天気＋ToDo（MVP）

[...短い説明...]

## 使用技術
| 分類 | 内容 |
|------|------|
| フロントエンド | HTML / CSS / JavaScript (Vanilla) |
| 外部API | OpenWeatherMap API |
```

#### **改善後の README（コピペOK）**

👇 以下の内容で README.md を上書き 👇

```markdown
# 🌤️ お天気＋ToDo アプリ

![Status](https://img.shields.io/badge/Status-完成-brightgreen)
![Completion](https://img.shields.io/badge/完成度-100%25-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 🎯 このアプリは何か？

毎日の**天気とタスク**を1つの画面で確認できるアプリです。

### 📱 こんなシーンで使えます
```
朝起きて...

従来：
  1. 天気アプリで「今日の天気は？」
  2. カレンダーアプリで「今日のタスクは？」
  → めんどくさい！

このアプリ：
  👉 1画面で「天気」も「タスク」も見れる！
```

---

## 💭 なぜ作ったのか？

**背景**：
- 天気予報を見る
- タスク管理をする

この2つは毎日一緒にやるのに、別々のアプリを使わなきゃいけない。
**不便だから、1つにまとめてみた！**

---

## 🎓 ここで学んだ技術

### 1️⃣ 外部API連携（OpenWeather API）
```javascript
// APIから天気データを取得
fetch(url)
  .then(response => response.json())
  .then(data => {
    console.log(data.main.temp);  // 気温
    console.log(data.weather[0].description);  // 天候
  });
```
✅ **学んだこと**
- APIの呼び出し方
- JSONデータの扱い方
- 非同期処理（fetch）

### 2️⃣ ローカルストレージ（データ保存）
```javascript
// タスクをブラウザに保存
localStorage.setItem('tasks', JSON.stringify(taskArray));

// 保存したデータを読み込む
const savedTasks = JSON.parse(localStorage.getItem('tasks'));
```
✅ **学んだこと**
- ページを閉じてもデータが残る仕組み
- JSONの保存と読み込み

### 3️⃣ レスポンシブ対応（スマホ対応）
```css
/* スマホで見やすいように */
@media (max-width: 768px) {
  .container {
    padding: 10px;
    font-size: 14px;
  }
}
```
✅ **学んだこと**
- PC・タブレット・スマホの3サイズ対応
- CSS メディアクエリの使い方

---

## 📊 完成度

| 機能 | 状態 | 説明 |
|------|------|------|
| ✅ タスク追加・削除 | **完成** | タスクの入力・削除ができます |
| ✅ タスク完了チェック | **完成** | チェックボタンで完了/未完了を切り替え |
| ✅ 天気情報表示 | **完成** | 気温・天候・気圧を表示 |
| ✅ 天気アイコン表示 | **完成** | 晴れ・雨などのアイコンを表示 |
| ✅ 都市名保存 | **完成** | デフォルト都市を設定できます |
| ✅ ローカルストレージ | **完成** | リロード後もデータが残ります |
| ✅ レスポンシブ対応 | **完成** | スマホでも快適に使えます |

---

## 🛠️ 使用技術

| 分類 | 技術 | 備考 |
|------|------|------|
| **フロントエンド** | HTML / CSS / JavaScript | フレームワークなしの Vanilla JS |
| **外部API** | OpenWeatherMap API | 天気情報の取得 |
| **データ保存** | LocalStorage | ブラウザ内に自動保存 |
| **デプロイ** | GitHub Pages | 無料でWebサイト公開 |
| **バージョン管理** | Git / GitHub | コード管理 |

---

## 📱 デモを試す

🔗 **[ここをクリックしてデモを見る](https://hikaru-taniguchi.github.io/weather-todo-app/)**

---

## 💻 コードを見る

🔗 **[GitHubでコードを確認](https://github.com/hikaru-taniguchi/weather-todo-app)**

---

## 🌈 今後の改善予定

- ⏰ **複数都市対応**: 複数の都市の天気を同時表示
- 🔔 **通知機能**: 「雨だから傘を持とう」などのアラート
- 📊 **グラフ表示**: タスク完了率をグラフで可視化
- ⚛️ **React版**: フレームワークを使った改良版

---

## 📄 ライセンス

MIT License - 自由に使ってOK！

---

## 👤 制作者

**谷口 輝 (Hikaru Taniguchi)**  
Webアプリ開発を学習中。日常の課題をITで解決するアプリ開発を目指しています。

---
```

#### ✅ 具体的にどう変更するか

1. GitHub で自分のリポジトリを開く
2. README.md をクリック
3. ✏️ **編集ボタン（鉛筆アイコン）**をクリック
4. 上の「改善後の README」をコピーして、全て貼り付け
5. 下にスクロール → **Commit changes** をクリック

---

### 🔧 手順2: Status Badge を追加

#### **やること**
README.md の一番上に、完成度バッジを表示する

#### **現在**
```markdown
# 🌤️ お天気＋ToDo（MVP）

![screenshot](assets/images/screenshot-hero.png)
```

#### **改善後**
```markdown
# 🌤️ お天気＋ToDo アプリ

![Status](https://img.shields.io/badge/Status-完成-brightgreen)
![Completion](https://img.shields.io/badge/完成度-100%25-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

![screenshot](assets/images/screenshot-hero.png)
```

#### 🎨 バッジの種類（選んで使えます）

```
✅ 完成した場合
![Status](https://img.shields.io/badge/Status-完成-brightgreen)

🔨 開発中の場合
![Status](https://img.shields.io/badge/Status-開発中-yellow)

🧪 試作段階の場合
![Status](https://img.shields.io/badge/Status-試作-orange)

❌ 停止中の場合
![Status](https://img.shields.io/badge/Status-停止-red)
```

---

### 🔧 手順3: .gitignore を確認

#### **何か？**
GitHub に**アップロードしてはいけないファイル**を指定

#### **確認方法**

1. リポジトリを開く
2. ファイル一覧から **.gitignore** を探す
   - あれば → ✅ OK
   - なければ → 作成が必要

#### **作成方法（.gitignore がない場合）**

1. **Add file** → **Create new file** をクリック
2. ファイル名に `.gitignore` と入力
3. 下の内容をコピペ

```
# Node modules（不要なファイル群）
node_modules/

# ログファイル
*.log
npm-debug.log

# 秘密情報（APIキーなど）
.env
.env.local

# エディタのキャッシュ
.vscode/
.idea/

# OS固有ファイル
.DS_Store
Thumbs.db

# ビルド結果
dist/
build/
```

4. **Commit changes** をクリック

---

### 🔧 手順4: GitHub Topics を設定

#### **何か？**
リポジトリに「タグ」をつけて、検索しやすくする

#### **やり方**

1. リポジトリのトップページを開く
2. 右上の **⚙️ Settings** をクリック
3. 左サイドバーで **Topics** を見つける
4. 以下を入力（複数入力可）

```
javascript
weather-app
todo
api
html-css
github-pages
```

5. **Save changes**

---

---

# 改善プロジェクト2️⃣

## 🧺 sentaku-biyori（洗濯アプリ）

### 📌 今の状態
```
✅ ユニークなコンセプト
✅ README はそこそこ充実している

❌ ただし、「学習ポイント」が不十分
❌ 「何が技術的にすごいのか」がわからない
```

### 🔴 問題点
- 「洗濯のタイミングを教えてくれるアプリ」はわかる
- でも「どうやって実装したのか」「何を学んだのか」が不明

---

### ✅ 改善方法

#### 改善後の README（コピペOK）

```markdown
# 🧺 せんたくびより

![Status](https://img.shields.io/badge/Status-完成-brightgreen)
![Completion](https://img.shields.io/badge/完成度-95%25-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

![センタクびより画面イメージ](./screenshot.png)

---

## 🎯 このアプリは何か？

**「今日、洗濯するなら何時がいい？」** を教えてくれるアプリです。

### 📱 こんな風に使います
```
朝 7:00
 ↓ アプリを開く
 ↓
 「今日は 14:00～17:00 が一番乾きやすい！」
 ↓
 その時間に洗濯する
 ↓ ✨
 早く乾いた！
```

---

## 💭 なぜ作ったのか？

**日常の不便さから生まれた**

毎日：
1. 天気予報を開く
2. 「気温どのくらい？湿度は？風は？」
3. 頭で計算...「この時間は乾きやすいかな？」

→ **毎日めんどくさい！**

そこで思いついた：
💡 「これ、アプリで自動計算できたら楽じゃん」

---

## 🎓 ここで学んだ技術

### 1️⃣ 独自アルゴリズム設計（スコア計算ロジック）

**洗濯に適した時間を判定する計算式**

```javascript
// 気温・湿度・風速・降水確率から「洗濯スコア」を計算

function calculateLaundryScore(temp, humidity, windSpeed, precipitation) {
  let score = 0;
  
  // 気温が高いほど良い（25～30℃が理想）
  if (temp > 25 && temp < 30) {
    score += 30;
  } else if (temp > 15) {
    score += 20;
  }
  
  // 湿度が低いほど良い（60%以下が理想）
  if (humidity < 60) {
    score += 30;
  } else if (humidity < 80) {
    score += 15;
  }
  
  // 風が強いほど良い（時速5m以上が理想）
  if (windSpeed > 5) {
    score += 30;
  } else if (windSpeed > 2) {
    score += 15;
  }
  
  // 雨が降らないほど良い
  if (precipitation < 10) {
    score += 10;
  }
  
  return score;
}
```

✅ **学んだこと**
- 複数の変数から1つの判定値を計算する方法
- ビジネスロジックの設計（「何を優先するか」の判定）
- スコアリングアルゴリズム

### 2️⃣ 3時間ごとの時系列データ処理

```javascript
// OpenWeather API から 3時間ごとのデータを取得
const forecastData = response.list;  // 40個分のデータ（5日間分）

// 時間ごとにスコアを計算
const scores = forecastData.map(item => ({
  time: new Date(item.dt * 1000),
  score: calculateLaundryScore(
    item.main.temp,
    item.main.humidity,
    item.wind.speed,
    item.rain?.['3h'] || 0
  )
}));

// 一番スコアが高い時間を見つける
const bestTime = scores.reduce((prev, current) => 
  (prev.score > current.score) ? prev : current
);
```

✅ **学んだこと**
- 時系列データの処理
- 配列操作（map, reduce）
- JSON形式のネストされたデータの取得

### 3️⃣ レスポンシブ設計（スマホファースト）

```css
/* デバイスごとに最適なレイアウト */

/* スマホ（デフォルト） */
.score-card {
  font-size: 18px;
  padding: 20px;
  width: 100%;
}

/* タブレット */
@media (min-width: 768px) {
  .score-card {
    font-size: 20px;
    padding: 30px;
  }
}

/* PC */
@media (min-width: 1024px) {
  .container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }
}
```

✅ **学んだこと**
- モバイルファーストの考え方
- CSS メディアクエリ
- 複数デバイスでの見え方の最適化

### 4️⃣ API の誤り処理（エラーハンドリング）

```javascript
// API 取得に失敗した場合、デモデータを表示

fetch(apiUrl)
  .then(response => {
    if (!response.ok) {
      throw new Error('API呼び出し失敗');
    }
    return response.json();
  })
  .catch(error => {
    console.error('エラー:', error);
    // デモデータを使う
    return demoData;
  });
```

✅ **学んだこと**
- try-catch とエラーハンドリング
- ユーザーフレンドリーな挙動（エラーでも壊れない）

---

## 📊 完成度

| 機能 | 状態 | 説明 |
|------|------|------|
| ✅ 天気データ取得 | **完成** | OpenWeather APIから取得 |
| ✅ スコア計算 | **完成** | 4要素から最適な時間を判定 |
| ✅ 時間ごと比較 | **完成** | 24時間の推移を表示 |
| ✅ 天気アイコン | **完成** | 晴れ・雨などのアイコン表示 |
| ✅ レスポンシブ対応 | **完成** | スマホ・タブレット・PC対応 |
| ✅ エラーハンドリング | **完成** | デモデータで常に動作 |
| ⚠️ 複数都市対応 | **開発中** | 今は1都市のみ |
| ⚠️ 登録機能 | **予定中** | よく使う都市を保存できるように |

---

## 🛠️ 使用技術

| 分類 | 技術 | 詳細 |
|------|------|------|
| **フロントエンド** | HTML / CSS / JavaScript | Vanilla JS（フレームワークなし） |
| **外部API** | OpenWeatherMap API | 5日間の天気予報データ |
| **データ構造** | JSON | 気象データの取得と処理 |
| **アルゴリズム** | スコアリング計算 | 独自ロジックで最適時間を判定 |
| **デプロイ** | GitHub Pages | 無料でホスティング |

---

## 📱 デモを試す

🔗 **[ここをクリックしてデモを見る](https://hikaru-taniguchi.github.io/sentaku-biyori/)**

**試し方**：
1. アプリを開く
2. 自分の都市を入力（例：札幌）
3. 「洗濯スコア」が表示される
4. 一番高い時間帯が「今日のおすすめ洗濯時間」

---

## 💻 コードを見る

🔗 **[GitHubでコードを確認](https://github.com/hikaru-taniguchi/sentaku-biyori)**

**主なファイル**：
- `index.html` - 画面構成
- `styles.css` - デザイン
- `app.js` - メインのロジック（スコア計算）

---

## 🌈 今後の改善予定

- 🌍 **複数都市対応**: よく使う都市を登録できるように
- 📊 **グラフ表示**: 24時間のスコア推移をグラフで表示
- 🔔 **通知機能**: 最適時間に通知を送る
- 📱 **PWA対応**: オフラインでも使えるように

---

## 📄 ライセンス

MIT License

---

## 👤 制作者

**谷口 輝 (Hikaru Taniguchi)**

工場での業務改善を通じて「課題解決」にやりがいを感じ、
プログラミングで日常の不便を改善するアプリ開発を目指しています。

---
```

#### ✅ 手順
- weather-todo-app と同じ方法で、README.md を上記に置き換え
- Status Badge を追加
- .gitignore を確認

---

---

# 改善プロジェクト3️⃣

## 🏔️ health-tracker-app（体調記録アプリ）

### 📌 今の状態
```
✅ 機能は動いている
✅ レスポンシブ対応している

❌ README が短い
❌ 「何を学んだのか」がない
❌ localStorage 未実装（まだやることがある）
```

### 🔴 問題点
- 「完成品」なのか「開発中」なのか不明
- localStorage が未実装なのに、README に書いていない

---

### ✅ 改善方法

#### 改善後の README（コピペOK）

```markdown
# 📊 体調記録アプリ

![Status](https://img.shields.io/badge/Status-開発中-yellow)
![Completion](https://img.shields.io/badge/完成度-80%25-yellow)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 🎯 このアプリは何か？

毎日の **体調・気分・生活習慣** を記録して、
**自分の「調子が良い・悪い」パターン**を発見するアプリです。

### 📱 使い方
```
毎日記録する：
 • 体調スコア（1～10）
 • 気分（いい・普通・悪い）
 • 昨日の飲酒（有・無）
 • 今日の飲酒（有・無）
 • しんどくなった理由
 • 楽になった理由

1ヶ月後...
 • 「金曜夜に飲むと、月曜日は最悪だな」
 • 「〇〇をするといつも調子いい」
 • こんなパターンが見える！
```

---

## 💭 なぜ作ったのか？

**背景**：
健康を改善するには「自分の行動と体調の関係」を知ることが重要。

でも実現するには：
- 毎日手書き記録 → 面倒くさい ❌
- 手書きを整理 → 時間がかかる ❌

→ **そこで、アプリなら簡単に記録・管理できる！**

---

## 🎓 ここで学んだ技術

### 1️⃣ JavaScript オブジェクト設計（データ構造）

```javascript
// 1日分のデータを「1つのオブジェクト」にまとめる
const dayRecord = {
  date: "2026-06-03",
  health: 7,          // 体調スコア
  mood: "good",       // 気分
  alcohol_yesterday: false,
  alcohol_today: false,
  hardPoints: ["仕事のストレス", "睡眠不足"],
  easyPoints: ["運動した", "瞑想した"]
};

// これを配列で管理
const allRecords = [
  dayRecord,  // 6月3日分
  {...},      // 6月2日分
  {...}       // ...
];
```

✅ **学んだこと**
- JSONライクなオブジェクト構造の設計
- 複数の属性をまとめる方法
- 配列でコレクション管理

### 2️⃣ DOM操作（画面の動的更新）

```javascript
// フォームから入力値を取得
const healthScore = document.querySelector('#health-input').value;
const mood = document.querySelector('input[name="mood"]:checked').value;

// 取得した値で画面を更新
const recordHTML = `
  <div class="record">
    <p>体調: ${healthScore}</p>
    <p>気分: ${mood}</p>
  </div>
`;
document.querySelector('#records-list').innerHTML += recordHTML;
```

✅ **学んだこと**
- getElementById / querySelector で要素を取得
- innerHTML でHTML生成・追加
- リアルタイムに画面更新

### 3️⃣ フォーム操作とデータ取得

```javascript
// フォーム送信イベント
document.querySelector('form').addEventListener('submit', function(e) {
  e.preventDefault();  // ページリロード防止
  
  // 入力値を取得
  const formData = new FormData(this);
  const data = Object.fromEntries(formData);
  
  // データ保存
  saveRecord(data);
  
  // フォーム初期化
  this.reset();
});
```

✅ **学んだこと**
- フォームイベントの処理
- FormData の使い方
- イベントバブリングの制御

### 4️⃣ レスポンシブ設計

```css
/* 毎日使うので、スマホでも見やすく */

.record-form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

@media (max-width: 768px) {
  .input-group {
    width: 100%;
    font-size: 16px;  /* iOS で自動ズーム回避 */
  }
}
```

✅ **学んだこと**
- モバイルファースト設計
- 入力フォームのモバイル最適化

---

## 📊 完成度

| 機能 | 状態 | 説明 |
|------|------|------|
| ✅ 記録フォーム | **完成** | 体調・気分・習慣を入力できます |
| ✅ 記録一覧表示 | **完成** | 記録した日付ごとにリスト表示 |
| ✅ 手動削除機能 | **完成** | 記録を削除できます |
| ✅ レスポンシブ対応 | **完成** | スマホ・タブレット・PC対応 |
| ✅ データ可視化 | **開発中** | 体調スコアのグラフ表示 |
| ⚠️ localStorage 保存 | **開発中** | ページ閉じてもデータが残るように（予定中） |
| ⚠️ エクスポート機能 | **予定中** | CSV出力で医師と相談できるように |

---

## 🛠️ 使用技術

| 分類 | 技術 | 詳細 |
|------|------|------|
| **フロントエンド** | HTML / CSS / JavaScript | Vanilla JS |
| **データ管理** | JavaScript オブジェクト・配列 | ブラウザ内でメモリ管理 |
| **DOM操作** | querySelector / innerHTML | 画面のリアルタイム更新 |
| **デプロイ** | GitHub Pages | 無料ホスティング |

---

## 📱 デモを試す

🔗 **[ここをクリックしてデモを見る](https://hikaru-taniguchi.github.io/health-tracker-app/)**

---

## 💻 コードを見る

🔗 **[GitHubでコードを確認](https://github.com/hikaru-taniguchi/health-tracker-app)**

---

## 🌈 今後の改善予定

### 🔴 優先度：高（今月中にやりたい）
- 📦 **localStorage 実装**: ページを閉じてもデータが残るように
- 📊 **グラフ表示**: 体調スコアの推移を可視化

### 🟡 優先度：中（学習が進んだら）
- 🔍 **検索・フィルター機能**: 日付や気分で検索
- 📈 **統計表示**: 「この1ヶ月の平均体調は?」

### 🟢 優先度：低（将来的に）
- ☁️ **クラウド保存**: 複数デバイスで同期
- 🔐 **ユーザー認証**: アカウント機能

---

## 📝 開発ノート

### なぜ localStorage はまだなのか？

**理由**：
1. 基本機能（記録・表示）をまず完成させることを優先
2. localStorage の実装は次のステップ
3. 焦ってコードが汚くなるより、段階的に進める

**実装予定**：6月中

```javascript
// 実装予定のコード
function saveToLocalStorage(records) {
  localStorage.setItem('healthRecords', JSON.stringify(records));
}

function loadFromLocalStorage() {
  const saved = localStorage.getItem('healthRecords');
  return saved ? JSON.parse(saved) : [];
}
```

---

## 📄 ライセンス

MIT License

---

## 👤 制作者

**谷口 輝 (Hikaru Taniguchi)**

工場での業務改善経験を通じて「課題解決」にやりがいを感じ、
プログラミングで日常の課題をITで改善することを目指しています。

---
```

#### ✅ 手順
- 同じ方法で README.md を置き換え
- ⚠️ Status を「開発中」にする（完成ではないため）
- 完成度を 80% に設定

---

---

# 改善プロジェクト4️⃣

## 🗺️ local-connection-app（地域マップアプリ）

### 📌 今の状態
```
✅ README が充実している
✅ 背景・ビジョンが明確

❌ 「試作段階」なのが不明確
❌ ファイルサイズが大きすぎる（8.9MB）
❌ 技術的なこだわりが見えない
```

### 🔴 問題点
- 素晴らしいコンセプトだが、「どこまで完成しているのか」が曖昧
- ファイルが重い → 開発環境に node_modules が含まれている可能性

---

### ✅ 改善方法

#### 改善箇所1: README の上部に Status と完成度を追加

**現在の README の先頭**
```markdown
# 🌿 地域創生 × IT
関係人口を生み出すマップ型サービス
**― 地図でつなぐ、地域と人の新しい関係 ―**
```

**改善後**
```markdown
# 🌿 地域創生 × IT

![Status](https://img.shields.io/badge/Status-試作-orange)
![Completeness](https://img.shields.io/badge/完成度-40%25-orange)
![License](https://img.shields.io/badge/license-MIT-blue)

関係人口を生み出すマップ型サービス  
**― 地図でつなぐ、地域と人の新しい関係 ―**
```

#### 改善箇所2: README に「現在の実装状況」セクションを追加

**追加する内容**（README のどこかに追加）

```markdown
## ⚙️ 現在の実装状況

### ✅ 完成している機能
- 🗺️ Leaflet での地図表示
- 📍 複数地点のマーカー表示
- 🌤️ OpenWeather API との連携（各地点の天気表示）
- 💾 JSON でのデータ管理

### 🔨 開発中の機能
- 📱 レスポンシブ対応（モバイルUI最適化）
- 🔍 検索・フィルター機能

### 📋 今後実装予定
- 👥 スキルマッチング機能
- 💬 コメント・レビュー機能
- 🔐 ユーザー認証
- ☁️ バックエンド構築

```

#### 改善箇所3: .gitignore を作成・改善

1. **リポジトリを開く**
2. **Add file** → **Create new file**
3. `.gitignore` と入力
4. 以下をコピペ

```
# Node modules
node_modules/
package-lock.json

# ログファイル
*.log
npm-debug.log

# 秘密情報
.env
.env.local

# エディタキャッシュ
.vscode/
.idea/
*.swp

# OS ファイル
.DS_Store
Thumbs.db

# ビルド結果
dist/
build/
```

5. **Commit changes**

---

---

# 改善プロジェクト5️⃣

## 📄 portfolio（メインのポートフォリオサイト）

### 📌 今の状態
```
✅ 複数プロジェクトを紹介している
✅ 背景も書いている

❌ このリポジトリの役割が曖昧（デプロイされている？）
❌ GitHub Pages で公開されているのか不明
❌ 全体的な構成が不明確
```

### 🔴 問題点
- portfolio というリポジトリが「何なのか」不明確
- 実際に GitHub Pages で公開されているのか不明確

---

### ✅ 改善方法

#### 手順1: ポートフォリオを GitHub Pages で公開

**確認方法**：

1. リポジトリの **Settings** を開く
2. 左メニューで **Pages** を見つける
3. 以下のように設定されているか確認

```
✅ Source: main ブランチ (root フォルダ)
✅ 公開URL: https://hikaru-taniguchi.github.io/portfolio
```

**もし設定されていなければ**：
1. **Source** を「main」に変更
2. **Save** をクリック
3. 5分待つ
4. URL が表示される

#### 手順2: README.md を改善

**改善後の README（コピペOK）**

```markdown
# 🎯 Hikaru Taniguchi - ポートフォリオ

![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue)
![Status](https://img.shields.io/badge/Status-公開中-brightgreen)

---

## 👋 こんにちは！

谷口輝と申します。  
札幌を拠点に、**日常の課題をプログラミングで解決する**ことに
やりがいを感じています。

---

## 📚 経歴

**工場での業務改善（2015～2024年）**
- Excel・Access を使った自動化・業務効率化
- 「仕組みで問題を解決する」ことの重要性を学ぶ

**IT分野への転身（2024年～）**
- プログラミングスキルを基礎から習得
- JavaScript / Web API を中心に学習中

---

## 🎓 スキル

### 言語・技術
| レベル | スキル |
|--------|--------|
| ⭐⭐⭐⭐⭐ | **HTML / CSS / JavaScript** |
| ⭐⭐⭐⭐ | **Web API 連携** (OpenWeather, Google Maps) |
| ⭐⭐⭐ | **LocalStorage / JSON** |
| ⭐⭐⭐ | **レスポンシブ Web デザイン** |
| ⭐⭐ | **Git / GitHub** |

### 今学んでいること
- Java / バックエンド開発
- データベース設計
- React / フレームワーク

---

## 🚀 作ったアプリ

### 1️⃣ 🌤️ お天気＋ToDo アプリ

**コンセプト**：毎日の天気とタスクを1画面で確認

- ✅ OpenWeather API で天気取得
- ✅ LocalStorage でタスク保存
- ✅ レスポンシブ対応

**技術ポイント**：非同期処理、DOM操作、データ永続化

🔗 [デモ](https://hikaru-taniguchi.github.io/weather-todo-app/) | 
🔗 [GitHub](https://github.com/hikaru-taniguchi/weather-todo-app)

![Status](https://img.shields.io/badge/Status-完成-brightgreen)

---

### 2️⃣ 🧺 センタクびより（洗濯アプリ）

**コンセプト**：天気データから「今日の最適な洗濯時間」を提案

- ✅ 気温・湿度・風速・降水確率から独自スコア計算
- ✅ 時間ごとの推移表示
- ✅ スマホUIの最適化

**技術ポイント**：アルゴリズム設計、時系列データ処理、API エラーハンドリング

🔗 [デモ](https://hikaru-taniguchi.github.io/sentaku-biyori/) | 
🔗 [GitHub](https://github.com/hikaru-taniguchi/sentaku-biyori)

![Status](https://img.shields.io/badge/Status-完成-brightgreen)

---

### 3️⃣ 📊 体調記録アプリ

**コンセプト**：毎日の体調・気分・生活習慣を記録して、
パターンを発見する

- ✅ 記録・表示・削除機能
- ✅ JSON形式のデータ構造設計
- ✅ レスポンシブ対応

**技術ポイント**：DOM操作、フォーム処理、オブジェクト設計

**今後**：localStorage 実装予定

🔗 [デモ](https://hikaru-taniguchi.github.io/health-tracker-app/) | 
🔗 [GitHub](https://github.com/hikaru-taniguchi/health-tracker-app)

![Status](https://img.shields.io/badge/Status-開発中-yellow)

---

### 4️⃣ 🗺️ 地域×情報マップ

**コンセプト**：地図上に地域情報と天気をまとめて表示し、
移住・地域理解のきっかけに

- 🗺️ Google Maps API での地図表示
- 📍 地域データの構造化（JSON）
- 🌤️ 地点ごとの天気表示

🔗 [デモ](https://hikaru-taniguchi.github.io/map_app/) | 
🔗 [GitHub](https://github.com/hikaru-taniguchi/map_app)

---

### 5️⃣ 🏔️ Local Connection App

**コンセプト**：地域の拠点・空き家を地図上に表示し、
「都市と地方のゆるいつながり」を設計

- 試作段階（開発中）
- Leaflet での地図表示
- JSONで地域データ管理
- 複数地点の天気表示

**ビジョン**：このアプリを通じて、関係人口を生み出し、
地域課題をITで解決する実証実験に

🔗 [デモ](https://hikaru-taniguchi.github.io/local-connection-app/) | 
🔗 [GitHub](https://github.com/hikaru-taniguchi/local-connection-app)

![Status](https://img.shields.io/badge/Status-試作-orange)

---

## 🎯 今後の目標

### 短期（3ヶ月）
- Java / バックエンド開発の基礎習得
- データベース設計の理解

### 中期（6ヶ月）
- React での Web アプリ開発
- バックエンド + フロントエンド統合

### 長期（1年）
- PM としてチーム開発に参画
- 地域課題解決のアプリを実運用する

---

## 📬 連絡先

- 📧 **Email**: rightgucci12@gmail.com
- 🐙 **GitHub**: https://github.com/hikaru-taniguchi
- 💼 **何かお仕事の相談があれば、お気軽に!**

---

## 📄 ライセンス

各プロジェクトは MIT License で公開しています。

---

**最終更新**: 2026年6月

```

#### ✅ 手順
1. portfolio リポジトリを開く
2. README.md の編集ボタンをクリック
3. 上記の内容に置き換え
4. Commit changes

---

---

# 📋 全体改善チェックリスト

## チェック: すべてのリポジトリ

```
❌ → ✅ に変えてください

リポジトリ: weather-todo-app
 [ ] README を改善版に置き換え
 [ ] Status Badge を追加
 [ ] .gitignore を確認
 [ ] GitHub Topics を設定: javascript, weather-app, todo, api

リポジトリ: sentaku-biyori
 [ ] README を改善版に置き換え
 [ ] Status Badge を追加
 [ ] .gitignore を確認
 [ ] GitHub Topics を設定: javascript, weather, algorithm, laundry

リポジトリ: health-tracker-app
 [ ] README を改善版に置き換え
 [ ] Status Badge を追加（開発中）
 [ ] .gitignore を確認
 [ ] GitHub Topics を設定: javascript, form, health-tracking

リポジトリ: local-connection-app
 [ ] README に Status Badge を追加
 [ ] README に「実装状況」を追加
 [ ] .gitignore を作成
 [ ] GitHub Topics を設定: javascript, map, leaflet, geospatial

リポジトリ: portfolio
 [ ] README を改善版に置き換え
 [ ] GitHub Pages が有効か確認
 [ ] portfolio を GitHub Pages で公開
 [ ] GitHub Topics を設定: portfolio, javascript, web-development
```

---

---

# 🎁 ボーナス：GitHub Topics の設定方法

### **なぜ Topics が大事？**
- 採用担当者が「javascript が得意な人」で検索したときに見つかる
- あなたの技術を「タグ」で表示できる

### **設定手順**

1. リポジトリを開く
2. 右上の **⚙️ Settings**
3. スクロール下して **Topics** を探す
4. 以下を追加：

**weather-todo-app の例**
```
javascript
weather-app
todo
api
local-storage
github-pages
```

5. Enter キーで追加
6. **Save changes**

---

---

# ✅ 最後に：チェックリスト（紙に印刷用）

## 今週やること

```
┌─────────────────────────────────────────┐
│ 🎯 今週の改善タスク                      │
└─────────────────────────────────────────┘

【優先度1】
□ weather-todo-app の README を置き換え
□ sentaku-biyori の README を置き換え
□ health-tracker-app の README を置き換え
  → 見積：1.5 時間

【優先度2】
□ portfolio の README を置き換え
□ portfolio を GitHub Pages で公開
  → 見積：30分

【優先度3】
□ 全リポジトリに .gitignore を確認・作成
□ 全リポジトリに GitHub Topics を設定
  → 見積：1時間

【合計】約 3 時間で完成！
```

---

## 効果（やると何が変わる？）

| 現在 | 改善後 |
|------|--------|
| 「え、何このアプリ？」 | 「あ、こんなことができるんだ！」 |
| 完成度が不明 | 「完成」「開発中」が一目瞭然 |
| 採用面接官の質問少ない | 「これどうやって実装したの？」と質問が増える |
| GitHub で見つかりにくい | 検索で見つかりやすくなる |

---

**頑張ってください！質問があればいつでも聞いてね。** 💪

