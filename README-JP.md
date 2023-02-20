# BATCAM FX Python Example

## 概要

このリポジトリは「BATCAM FX」開発に必要なWebSocket接続および、送信されるBF Dataを視覚化するメソットを含む例です。

コード作成時に添付の資料を参考までにお願いいたします。

## 実行

Pythonがインストール済みの環境で`requirements.txt`に記載されているDependency類をインストールします。2023年2月20日基準, <u>numba</u>はPython 3.11では作動しません。

コードを実行する前に、`websocket-client.py`内の以下の項目を修正する必要があります。
```python
user = ""
password = ""
camera_ip = ""
```

提供されたユーザー名とパスワード、そしてカメラのIPアドレスを入力し、Pythonで`Websocket-client.py`を実行します。
```sh
python websocket-client.py
```

## 注意

このリポジトリで提供するサンプルコードには以下の限界事項がございます。

* WebSocket接続解除時、再接続不可
* matplotlibのimshow性能issueによる25FPSの維持不可

## 開発環境

* macOS Ventura 13.2 (Darwin Kernel Version 22.3.0: Thu Jan  5 20:48:54 PST 2023; root:xnu-8792.81.2~2/RELEASE_ARM64_T6000 arm64)
* Python 3.9.13

その他Python Dependencyに関する内容はrequirements.txtをご参考ください。