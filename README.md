# AiB-RP4

라즈베리파이 GPIO 제어를 위한 펠티어 소자 제어 시뮬레이션 도구입니다.

## 개요

CSV 파일에 정의된 시나리오에 따라 펠티어 소자의 전원 및 방향을 제어하는 시뮬레이션 프로그램입니다. 실제 라즈베리파이 하드웨어가 없는 환경에서도 테스트할 수 있도록 FakeRPi를 사용합니다.

## 주요 기능

- CSV 파일 기반 시나리오 실행
- 펠티어 소자 전원 제어 (GPIO HIGH/LOW)
- 펠티어 소자 방향 제어 (상승/하강)
- 랜덤 시퀀스 기반 제어

## 사용 방법

```bash
python test.py
```

## 요구사항

- Python 3.12
- FakeRPi (라즈베리파이 하드웨어가 없는 경우)

## 설치

### uv 설치

#### Windows
```powershell
# PowerShell에서 실행
irm https://astral.sh/uv/install.ps1 | iex
```

#### macOS / Linux
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

설치 후 터미널을 재시작하거나 다음 명령어로 PATH에 추가:
```bash
export PATH="$HOME/.cargo/bin:$PATH"
```

### 가상환경 설정

```bash
# Python 3.12 가상환경 생성
uv venv --python 3.12

# 가상환경 활성화
# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# macOS / Linux
source .venv/bin/activate
```

### 패키지 설치

```bash
# uv를 사용한 패키지 설치
uv pip install -r requirements.txt
```

## 파일 구조

- `test.py`: 메인 스크립트
- `test_scenario.csv`: 제어 시나리오 파일 (Power, Direction 컬럼 포함)

## 참고

- 실제 라즈베리파이 하드웨어를 사용하는 경우 `FakeRPi` 대신 `RPi.GPIO`를 사용하세요.
- GPIO 핀 설정은 코드 내에서 수정 가능합니다.

---

해당 프로젝트는 Examples-Python의 Private Repository에서 공개 가능한 수준의 소스를 Public Repository로 변환한 것입니다.

