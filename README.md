# order-notifier (開発初期段階)

## 開発環境のインストール

- [tailwindcss のインストール](https://tailwindcss.com/blog/standalone-cli)

```
$ target=linux-x64 # or linux-arm{64,v7}, macos-{arm,x}64, windows-{arm,x}64.exe
$ curl -sLO https://github.com/tailwindlabs/tailwindcss/releases/latest/download/tailwindcss-${target}
$ chmod u+x tailwindcss-${target}
$ ln -sf tailwindcss-${target} tailwindcss
```

- [rye](https://rye.astral.sh/) を用いて venv 環境の構築

```
$ rye sync --no-lock
```

### 開発環境

テンプレートファイルの変更に応じてCSSを生成する:

```
$ rye run tailwind-watch
```

別のttyで、開発Webサーバーを立ち上げる:

```
$ source .venv/bin/activate
$ rye run watch
```

- /docs でAPIの仕様が見れて、リクエストを投げることもできる
- /order が（今の所）メインの画面

### 本番環境

```
$ rye run tailwind-build
$ rye run serve
```

## 参考リンク

htmx

- https://htmx.org/docs/

tailwindcss

- https://tailwindcss.com/docs/utility-first

Python

- https://fastapi.tiangolo.com/
- https://mypy.readthedocs.io/en/latest/cheat_sheet_py3.html
- https://www.encode.io/databases/
- https://docs.sqlalchemy.org/en/20/core/
- https://jinja.palletsprojects.com/en/3.1.x/
