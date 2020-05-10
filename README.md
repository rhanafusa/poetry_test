# poetryを利用した環境構築

## poetryのインストールと設定

poetryをインストールしてください。

Linuxの場合

```console
curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python
```

Windowsの場合（powershellを使用）

```powershell
(Invoke-WebRequest -Uri https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py -UseBasicParsing).Content | python
```

その他のインストール方法は[poetryのドキュメント](https://python-poetry.org/docs/)を参照してください。

poetryのインストール完了後、以下のコマンドでpoetryの設定変更を行ってください。プロジェクトディレクトリ内にpython仮想環境を作成します。プロジェクトディレクトリ外にあると管理しづらいためです。

```console
poetry config virtualenvs.in-project true
```

## 環境構築

gitリポジトリをクローンしてください。

```console
git clone git@github.com:rhanafusa/poetry_test.git
```

クローンしたリポジトリに移動し、`poetry install`で環境を構築します。

```console
cd poetry_test
poetry install
```

## notebookを開く

環境構築終了後、以下のコマンドで`jupyter notebook`を起動してください。`poetry`で構築したpython仮想環境の`jypyter notebook`を実行します。

```console
poetry run jupyter notebook
```

自動的にブラウザで開かれます。ブラウザの画面で`poetry_test/python_environment_instruction.ipynb`を開いてください。
自動的に`jupyter notebook`が開かれない場合、コンソールに表示されたURLにアクセスしてください。
