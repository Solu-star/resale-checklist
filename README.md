# 中古せどりチェックリスト 公開用

公開ページ:

https://solu-star.github.io/resale-checklist/

GitHubリポジトリ:

https://github.com/Solu-star/resale-checklist

## 使い方

- スマホでは公開URLをブックマーク、またはホーム画面に追加して使う。
- 内容を更新したら `index.html` を編集してGitHubへ反映する。
- 画面右上の「更新」ボタンで、スマホ側のキャッシュを避けて読み直せる。

## 他のPCで作業を続ける方法

1. GitHubにログインできるPCでターミナルを開く。
2. 作業したいフォルダへ移動する。
3. 次のコマンドでリポジトリを取得する。

```bash
git clone https://github.com/Solu-star/resale-checklist.git
cd resale-checklist
```

4. `index.html` を編集する。
5. ローカルで確認する。

```bash
python3 -m http.server 8765
```

ブラウザで `http://127.0.0.1:8765/` を開く。

6. 問題なければGitHubへ反映する。

```bash
git status
git add index.html README.md
git commit -m "Update checklist"
git push
```

7. 数十秒から数分後に公開ページへ反映される。

## 更新するときの注意

- `index.html` の `dataUpdatedAt` を更新日時に合わせて変更する。
- スマホで古い表示が残る場合は、画面上部の「更新」ボタンを押す。
- 変更前に `git pull` してから作業すると、他PCでの変更とぶつかりにくい。

```bash
git pull
```

## 注意

- 公開URLを知っている人は閲覧できるため、仕入れノウハウを完全に非公開にしたい場合は、パスワード付きの公開先を使う。
