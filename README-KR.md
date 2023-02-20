# BATCAM FX Python Example

## 개요

이 레포지터리는 BATCAM FX 개발에 필요한 WebSocket 연결과 BATCAM FX 에서 전달되는 BF Data 를 시각화하는 메소드를 포함하는 예제입니다.

제공된 문서와 같이 코드를 참조하시기 바랍니다.

## 실행

Python 이 설치된 컴퓨터에서, 편한 방법으로 `requirements.txt` 파일에 명시된 Dependency 들을 설치합니다. 2023년 2월 20일 기준, <u>numba</u>는 현재 Python 3.11 에서 작동하지 않으므로 참고하시기 바랍니다.

코드를 실행하기 전에, `websocket-client` 내의 인자들을 수정해야 합니다.
```python
USER = ""
PASSWORD = ""
CAMERA_IP = ""
```

제공받은 사용자명과 비밀번호, 그리고 카메라의 주소를 입력하고, python을 통해 `websocket-client.py` 를 실행합니다.
```sh
python websocket-client.py
```

## 한계

이 레포지터리에서 제공하는 예제 코드는 다음과 같은 한계 사항을 가지고 있습니다:

* WebSocket 연결 해제 시 재연결 불가
* matplotlib 의 imshow 성능 이슈에 따른 초당 25 프레임 유지 불가능

## 개발 환경

* macOS Ventura 13.2 (Darwin Kernel Version 22.3.0: Thu Jan  5 20:48:54 PST 2023; root:xnu-8792.81.2~2/RELEASE_ARM64_T6000 arm64)
* Python 3.9.13

기타 Python Dependency에 관한 사항은 `requirements.txt` 파일을 참조하세요.