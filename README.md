# AI 학습의 수학적 기반

NumPy로 선형대수, 미적분, 역전파, 최적화, 확률·통계를 학습하는 과제입니다.
주피터 노트북을 중심으로 작업하며, 그래프는 Matplotlib과 Seaborn으로 그립니다.

## 환경 설치

Python 3.13과 [uv](https://docs.astral.sh/uv/)를 사용합니다.
프로젝트 루트에서 다음 명령을 실행하면 `.venv`에 잠긴 버전의 의존성을 설치합니다.
Python 3.13이 없다면 uv가 자동으로 설치합니다.

```sh
uv sync --locked
```

- 계산·시각화: NumPy, Matplotlib, Seaborn
- 노트북 도구 (`dev` 그룹, 기본 설치): JupyterLab, ipykernel

`pyproject.toml`에서 의존성을 관리하고 `uv.lock`으로 정확한 버전을 고정합니다.
과제 제출용 `requirements.txt`에는 직접 사용하는 계산·시각화 라이브러리
NumPy, Matplotlib, Seaborn의 버전만 기록합니다.
노트북 도구는 `pyproject.toml`의 `dev` 그룹에서 관리합니다.

## 노트북 실행

```sh
uv run jupyter lab
```

브라우저에서 노트북을 만들고 프로젝트 `.venv`의 Python 커널을 선택합니다.
VS Code에서는 노트북의 **Select Kernel → Python Environments**에서
`.venv/bin/python`을 선택합니다. 가상환경을 별도로 활성화할 필요는 없습니다.

## 의존성 변경

```sh
uv add 패키지이름
uv add --dev 개발도구이름
```

계산·시각화 라이브러리를 추가하거나 버전을 변경했다면 `uv.lock`에 기록된
버전으로 `requirements.txt`의 직접 의존성 목록도 함께 갱신합니다.
