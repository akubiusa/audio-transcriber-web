# GitHub Copilot Instructions

## プロジェクト概要
Web-based audio transcription tool using browser's SpeechRecognition API to transcribe microphone input with optional API POST.

## 共通ルール
- 会話は日本語で行う。
- PR とコミットは Conventional Commits に従う。
- PR タイトルとコミット本文の言語: PR タイトルは Conventional Commits 形式（英語推奨）。PR 本文は日本語。コミットは Conventional Commits 形式（description は日本語）。
- 日本語と英数字の間には半角スペースを入れる。
- 既存のプロジェクトルールがある場合はそれを優先する。

## 技術スタック
- 言語: Python, JavaScript, HTML
- パッケージマネージャー: pip

## コーディング規約
- フォーマット: 既存設定（ESLint / Prettier / formatter）に従う。
- 命名規則: 既存のコード規約に従う。
- Lint / Format: 既存の Lint / Format 設定に従う。
- コメント言語: 日本語
- エラーメッセージ: 英語
- TypeScript 使用時は strict 前提とし、`skipLibCheck` で回避しない。
- 関数やインターフェースには docstring（JSDoc など）を記載する。

### 開発コマンド
```bash
# install
pip3 install -U -r requirements.txt

# run
python3 main.py --open-browser

# server
uvicorn application:app

```

## テスト方針
- 新機能や修正には適切なテストを追加する。

## セキュリティ / 機密情報
- 認証情報やトークンはコミットしない。
- ログに機密情報を出力しない。

## ドキュメント更新
- 実装確定後、同一コミットまたは追加コミットで更新する。
- README、API ドキュメント、コメント等は常に最新状態を保つ。

## リポジトリ固有
- **type**: Web Application
**features:**
  - Real-time microphone transcription
  - Optional API URL posting
  - localStorage settings persistence (API URL, AutoStart)
  - Sentence alternatives with hover diff visualization
  - Manual recording start/stop
**browsers_supported:**
  - Chrome 33+
  - Edge 79+
**deployment_options:**
  - Local Python server
  - Remote PHP API endpoint