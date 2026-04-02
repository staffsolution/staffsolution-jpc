# GitHub Pages セットアップ手順（JPC グルコン）

## 1. GitHubで新しいリポジトリを作る

1. https://github.com/new を開く
2. 以下の設定で作成：
   - **Repository name**: `staffsolution-jpc`
   - **Visibility**: Private（メンバー限定公開にしたい場合）または Public
   - README は不要（チェックしない）
3. 「Create repository」をクリック

## 2. このフォルダ（docs-jpc）を push する

ターミナルで以下を実行：

```bash
cd /Volumes/OWC\ Envoy\ Pro\ FX/w-work/s-スタッフソリューション/staffsolution_cursor

# docs-jpc を独立したリポジトリとして初期化
cd docs-jpc
git init
git add .
git commit -m "初回：JPC グルコン議事録サイト"
git branch -M main
git remote add origin https://github.com/staffsolution/staffsolution-jpc.git
git push -u origin main
```

## 3. GitHub Pages を有効にする

1. `https://github.com/staffsolution/staffsolution-jpc` を開く
2. **Settings → Pages**
3. Source を「Deploy from a branch」
4. Branch: `main` / Folder: `/ (root)`
5. 「Save」

## 4. 公開URL

設定後 1〜2 分で以下で公開されます：

```
https://staffsolution.github.io/staffsolution-jpc/
```

---

## 議事録を追加するときの手順

1. `docs-jpc/` フォルダ内に MD ファイルを置く
   - 例：`docs-jpc/20260402_グルコン議事録.md`
2. `docs-jpc/index.md` にリンクを追記する
3. このフォルダで `git add . && git commit -m "議事録追加" && git push`

これだけでサイトに自動反映されます。
