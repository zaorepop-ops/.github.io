# ブロスタ キャラクター当てクイズ（静的サイト）

画像を見てブロスタのキャラクターを当てる 4 択クイズです。  
**プレーンな HTML / CSS / JavaScript** だけで動作し、**GitHub Pages** で公開できます（Django は不要です）。

## 公開 URL（Pages）

マージ後・Pages 有効化後:

**https://zaorepop-ops.github.io/brawl-quiz/**

## GitHub Pages の有効化

まだ有効でない場合:

1. リポジトリの **Settings → Pages**
2. **Source**: Deploy from a branch
3. **Branch**: `main` / **Folder**: `/ (root)`
4. Save

数分待つと上記 URL でクイズが開きます。

## ローカルで確認

静的ファイルだけなので、ルートで簡易サーバを立てるだけで OK です。

```bash
# 例: Python
python3 -m http.server 8080
# ブラウザで http://127.0.0.1:8080/
```

主なファイル:

- `index.html` — 画面
- `styles.css` — スタイル
- `script.js` — クイズロジック（BrawlAPI からロースター取得）
- `characters.js` — 日本語表示名・除外・追加キャラなど

## Django アーカイブ

以前の Django 版は削除せず **`archive/django/`** に退避してあります。  
履歴は git に残っています。ローカルで Django を動かす場合はそちらを参照してください。

## その他

- Character DB 関連の PR 作業は別ブランチ／未マージです（この静的サイト本体とは独立）。
- `legacy_static/` はポインタ用です。正規の静的ファイルは **リポジトリ直下** にあります。
