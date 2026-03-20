<div align="center">

# 📜 Papyrus (パピルス)

[![GitHub Stars](https://img.shields.io/github/stars/Alpaca233114514/Papyrus?style=flat-square&logo=github&color=yellow)](https://github.com/Alpaca233114514/Papyrus/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Alpaca233114514/Papyrus?style=flat-square&logo=github&color=blue)](https://github.com/Alpaca233114514/Papyrus/forks)
[![GitHub Issues](https://img.shields.io/github/issues/Alpaca233114514/Papyrus?style=flat-square&logo=github&color=red)](https://github.com/Alpaca233114514/Papyrus/issues)
[![GitHub License](https://img.shields.io/github/license/Alpaca233114514/Papyrus?style=flat-square&color=green)](https://github.com/Alpaca233114514/Papyrus/blob/main/LICENSE)
[![Release](https://img.shields.io/github/v/release/Alpaca233114514/Papyrus?style=flat-square&logo=github&color=orange)](https://github.com/Alpaca233114514/Papyrus/releases)

![Minecraft Paper](https://img.shields.io/badge/Icon-Minecraft_Paper-green?style=flat-square)
![Python](https://img.shields.io/badge/Python-3.8-blue?style=flat-square&logo=python)
![AI-Assisted](https://img.shields.io/badge/Dev-AI--Assisted-blueviolet?style=flat-square)

**🌐 言語 / Languages / 语言:**
[日本語](README_JP.md) | [English](README.md) | [简体中文](README_ZH.md)

</div>

---

**Papyrus** は、高強度なモデル記憶に特化した、ミニマリストで効率的、キーボード駆動のAI Agent対応SRS（間隔反復システム）復習エンジンです。

> "大道は至りて簡なり。"

---

## ✨ 主な機能

- 🚀 **ミニマリストな操作**: 完全キーボード駆動のワークフロー、マウス不要。深い復習の「フロー状態」への入りを助けます。
- 🧠 **インテリジェントなスケジューリング**: エビングハウスの忘却曲線ロジックに基づいた簡易型間隔反復アルゴリズムを内蔵。習熟度に応じて次の復習を自動スケジュールします。
- 📦 **軽量・ポータブル**: 単一の `.exe` ファイル、ゼロ依存。データはローカルの `Papyrusdata.json` に保存され、プライバシーとセキュリティを確保。

---

## ⌨️ ショートカット (フローモード)

| キー | アクション | 効果 |
| :--- | :--- | :--- |
| **Space** | **答えを表示** | 巻物を展開して答えを見る |
| **1** | **忘れた** | 不明瞭としてマーク、短期間で高頻度復習 |
| **2** | **曖昧** | 不確かとしてマーク、後で再復習 |
| **3** | **習得済み** | 記憶が確実、復習間隔が線形に倍増 |

---

## 📥 一括インポート形式

`UTF-8` エンコーディングの `.txt` ファイルを以下の形式で準備してください：

```text
モデルシナリオまたは問題 A === コアトリガーまたは答え A

モデルシナリオまたは問題 B === コアトリガーまたは答え B
```

*ヒント：各カードは `===` で区切られます。明確さのため、グループ間に空行を入れることをお勧めします。*

---

## 🚀 ダウンロードと使用方法

### 1. プログラムの取得
[Releases](https://github.com/Alpaca233114514/Papyrus/releases) ページから最新バージョンをダウンロードしてください。

### 2. 実行手順
1. ダウンロードした `.zip` ファイルを任意のフォルダに展開します。
2. `Papyrus.exe` をダブルクリックして起動します。
> **注意：** `.exe` だけを他の場所に移動しないでください。そうしないと、アイコンや以前の復習進度を読み込めなくなります（v1.0.0のみ）。

### 3. AI機能の使用

#### 1. APIの設定
サイドバーの "⚙️ 設定" ボタンをクリックし、API Keyを入力してください：

- **OpenAI**: https://platform.openai.com/api-keys で取得
- **Anthropic**: https://console.anthropic.com/ で取得
- **Ollama**: ローカル実行、API Key不要
  ```bash
  # Ollamaのインストール
  # ダウンロード: https://ollama.ai
  
  # モデルのプル
  ollama pull llama2
  ```

#### 2. モード設定
**Agentモード**: AIがツール呼び出しを使用してカードの追加、編集、削除などを行います  
**Chatモード**: チャット機能のみ

#### 3. パラメータ調整
設定で以下を調整できます：
- **Temperature**: 創造性を制御（0-2、高いほどランダム）
- **Max Tokens**: 最大応答長

### 設定ファイル

AI設定は `data/ai_config.json` に保存され、以下を含みます：
- APIキー
- モデル選択
- パラメータ設定

### 注意事項

1. **API費用**: OpenAIとAnthropicは使用量に応じて課金されます。予算を設定することをお勧めします。
2. **ローカルモデル**: Ollamaは完全無料ですが、より良いハードウェアが必要です。
3. **ネットワーク**: クラウドAPIは安定したインターネット接続が必要です。
4. **プライバシー**: ローカルモデルのデータはアップロードされません。クラウドAPIは質問内容を送信します。

### トラブルシューティング

**AI機能が動作しない**
- `requests` ライブラリがインストールされているか確認
- コンソールのエラーメッセージを確認

**API呼び出し失敗**
- API Keyが正しいか確認
- ネットワーク接続を確認
- APIクォータが十分か確認

**Ollama接続失敗**
- Ollamaサービスが実行中か確認
- ポートが11434か確認
- 試す: `ollama serve`

---

## 🛠️ 技術詳細 (開発者向け)

- **開発モード**: 人間主導、AI補助 (Claude Sonnet 4.6, Gemini 3.0 Pro)
- **言語**: Python 3.8 (Tkinter)
- **エンジニアリング**: `PyInstaller` でパッケージ化、`sys._MEIPASS` リソースパス互換性を処理
- **ライセンス**: MIT License
- **クレジット**: アイコン素材は Minecraft Wiki (Mojang Studio) より

---

## 💡 開発者の言葉

この作品の誕生は、それほど理想的でも壮大でもありませんでした。

なぜ作ったのか？ある日、AIの学習をしていて、Ankiをダウンロードして知識を暗記しようとしました。ダウンロード後、アップデート確認が必要で、サーバーに接続する必要がありましたが、どうしても接続できませんでした。

そこでGeminiがそばにいるのに気づき、書いてもらうことにしました。いくつか調整して、使い始めました。

実は、もともとこれを公開するつもりはありませんでした。なぜ最終的に公開したのか？

昨日、久しぶりに古いアカウントで彼女のリポジトリにスターを付けたら、GitHubにボットと判断され、活動が削除されました。怒りました！私はAIを使いますが、私自身はAIではありません。AIではないことを証明するために、ちょうど手元にこれがあったので、磨き上げて公開しました。

話は終わりです。もう旧暦の6日目、もうすぐ夜明けです。苦学生、はぁ、ここで愚痴を言うしかありません。

私はこんな言葉が好きです：「知識は人を自由にする」(Veritas vos liberabit)。伟大な開発者の皆さんと共に、これは私の最初のオープンソースプロジェクトです。どうか温かく見守ってください。

遅ればせながら、新年の挨拶とさせていただきます。  
**新しい一年で、知識の刃を手に、夜の廃墟を突き破り、黎明の領域へと至らんことを。**

---

## 📚 ドキュメントナビゲーション

- [クイックスタートガイド](docs/guides/QUICKSTART.md) - 5分で始める
- [バージョン情報](docs/guides/VERSION.md) - 現在のバージョンと更新内容
- [変更履歴](docs/guides/CHANGELOG.md) - 完全なバージョン履歴
- [プロジェクト構造](docs/PROJECT_STRUCTURE.md) - コード構成
- [AI機能](docs/AI_README.md) - AIアシスタントガイド
- [AIツールデモ](docs/AI_TOOLS_DEMO.md) - 実際の使用例

---

<div align="center">

⭐ **このリポジトリが役に立ったら、Starをお願いします！** ⭐

[バグ報告](https://github.com/Alpaca233114514/Papyrus/issues) · [機能リクエスト](https://github.com/Alpaca233114514/Papyrus/issues) · [リリース](https://github.com/Alpaca233114514/Papyrus/releases)

</div>
