# 🎤 歌枠セトリ自動生成ツール (YouTube Setlist Generator)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/zero0r0/GetSongSetListTool/blob/main/SONG.ipynb)

推し活をエンジニアリングで解決！
YouTubeの「歌枠」アーカイブ動画から、Gemini APIを用いてタイムスタンプ付きのセットリスト（曲名 / アーティスト名）を全自動で生成するツールです。
環境構築は一切不要で、ブラウザ（Google Colab）上ですぐに実行できます。

## ✨ 特徴 (Features)
* **完全無料・環境構築不要**: Google Colab上で動作するため、PCでもスマホからでも実行可能です。
* **高精度なLLM解析**: `Gemini 2.5 Flash` を採用し、長時間配信でも高速かつ高精度に楽曲情報を抽出します。
* **重複・ノイズの自動排除**: セグメント境界で発生する曲の重複や、表記揺れを自動で整形・校正します。
* **ローカル分割による高速化**: `yt-dlp` と `ffmpeg` を用いて音声を一度だけダウンロード・分割することで、APIへの通信負荷と時間を最小限に抑えています。

## 🚀 使い方 (Usage)

本ツールを使用するには、無料のGoogleアカウントとGemini APIキーが必要です。

1. **APIキーの取得**
   [Google AI Studio](https://aistudio.google.com/app/apikey) にアクセスし、「Create API Key」から無料のAPIキーを取得します。
2. **ツールの起動**
   上記の `Open in Colab` ボタンをクリックしてツールを開きます。
3. **APIキーの設定**
   Colab画面左側の「鍵マーク🔑（シークレット）」を開き、名前に `GEMINI_API_KEY`、値に取得したAPIキーを貼り付けて保存します。
4. **URLを入力して実行**
   右側のフォームにYouTubeのURLを入力し、実行ボタン（▶）を押します。処理が完了すると、自動的に `setlist.txt` がダウンロードされます。

## ⚠️ 注意事項・免責事項 (Disclaimer)
* 本ツールは、著作権法第30条の4（情報解析のための利用）に基づいた技術検証および私的利用を目的としています。
* ツールの実行に伴うYouTube利用規約への抵触リスク等は、利用者自身の責任（自己責任）において管理してください。本ツールの作者は、いかなるトラブルや損害についても一切の責任を負いません。
* 長時間の動画（6時間以上など）や、ボット検知が厳しい動画の場合や、短期間でのアクセスを繰り返す等でエラーが発生することがあります（`cookies.txt` をアップロードすることで回避できる場合があります）。

## 📖 開発の背景・技術解説
本ツールの開発の裏側、AI（Gemini）との試行錯誤のプロセスについては、以下の技術ブログにまとめています。
* [【Zenn】推し活をエンジニアリングで解決する。Gemini API × Pythonで作る「歌枠セトリ自動生成ツール」を作ってみた件について](https://zenn.dev/zero_0r0/articles/0d685208754b68)

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
