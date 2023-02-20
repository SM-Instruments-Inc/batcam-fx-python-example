# BATCAM FX Python Example

한국어 README는 [여기](README-KR.md)에서 확인할 수 있습니다.<br>
日本語のREADMEは[こちら](README-JP.md)

## Summary

This repository provides an example of a WebSocket connection required for BATCAM FX development, and method for visualizing BF Data sent from BATCAM FX.

Please refer to the code with provided documentation.

## Execute

From PC with Python installed, install dependencies with `requirements.txt` file. Please note that <u>numba</u> is not currently support Python 3.11 for now. (Feb 20, 2023)

Before executing code, you should edit parameters in `websocket-client.py`
```python
USER = ""
PASSWORD = ""
CAMERA_IP = ""
```

Edit `websocket-client.py` with provided username, password and camera ip address, run `websocket-client.py` with Python.
```sh
python websocket-client.py
```

## Limitation

The example code provided in this repository has the following limitations:

* Unable to reconnect when WebSocket has disconnected.
* Due to matplotlib's imshow performance, the overlaying frame can't keep up 25 frames per second.

## Development Environment

* macOS Ventura 13.2 (Darwin Kernel Version 22.3.0: Thu Jan  5 20:48:54 PST 2023; root:xnu-8792.81.2~2/RELEASE_ARM64_T6000 arm64)
* Python 3.9.13

For other Python dependencies, see the `requirements.txt` file.