# FeatherPDF 🪶

**FeatherPDF** は、サーバーレスで動作する軽量なPDF編集ツールです。
Pythonの `pypdf` ライブラリと `Stlite` (Streamlit for WebAssembly) を使用しており、すべての処理がブラウザ内で完結します。

## 特徴
- **完全ローカル処理**: アップロードしたPDFファイルが外部サーバーに送信されることはありません。
- **サーバーレス**: 単一の `index.html` ファイルのみで動作します。
- **機能**:
  - ページの並べ替え
  - ページの削除
  - PDFの結合（アップロードしたファイルのページを選択して新しいPDFを作成）

## 使い方
1. [GitHub Pages](https://kazuki.github.io/feather-pdf/) (リンクはリポジトリ作成後に有効になります) にアクセスするか、`index.html` をダウンロードしてブラウザで開きます。
2. PDFファイルをドラッグ＆ドロップでアップロードします。
3. ページの順序を変更したり、不要なページを削除したりします。
4. 「PDFを処理する」ボタンをクリックします。
5. 処理されたPDFをダウンロードします。

## 技術スタック
- **Frontend/Runtime**: [Stlite](https://github.com/whitphx/stlite) (Streamlit running in the browser)
- **PDF Processing**: [pypdf](https://pypdf.readthedocs.io/en/latest/)
- **Language**: Python (running on Pyodide via WebAssembly)

## 開発
このプロジェクトは単一の `index.html` ファイルで構成されています。
開発を行うには、ローカルサーバーを立ち上げて `index.html` をホストすることをお勧めします（StliteのWASMワーカーが正しくロードされるため）。

```bash
python3 -m http.server 8080
```

ブラウザで `http://localhost:8080` にアクセスしてください。

## ライセンス
MIT License
