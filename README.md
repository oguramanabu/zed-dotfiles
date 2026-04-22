# zed-dotfiles

Zed editor の設定ファイル群。

## 構成

```
zed-dotfiles/
└── zed/
    └── snippets/
        └── c++.json    # AtCoder 用テンプレ & アルゴリズム snippet
```

## c++.json の置き場所

実運用では `~/.config/zed/snippets/c++.json` を Zed が読みにいく。
この repo の `zed/snippets/c++.json` は **バックアップ用のミラー**。
`atcoder-snippet-register` スキルが snippet を更新するたびに自動で
ここにコピー＋commit＋push される。

## 手動で同期したいとき

```bash
cp ~/.config/zed/snippets/c++.json ~/zed-dotfiles/zed/snippets/c++.json
cd ~/zed-dotfiles
git add -A
git commit -m "Update snippets manually"
git push
```

## 復旧手順

もし `~/.config/zed/snippets/c++.json` を消してしまったら:

```bash
cp ~/zed-dotfiles/zed/snippets/c++.json ~/.config/zed/snippets/c++.json
```

そして Zed で `cmd+shift+P` → `snippets: configure snippets` → `C++` を選んでタブを閉じれば再認識される。
