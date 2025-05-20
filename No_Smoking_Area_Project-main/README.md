# 🚭 Smoking Detection System Project  

---

## 📦 프로젝트 개요

본 프로젝트는 **YOLOv5 기반의 흡연자 탐지 시스템**으로,  
Flask 서버와 웹캠 스트리밍을 활용하여 **금연 구역 내 실시간 흡연 여부를 감지**하고,  
로그 및 통계를 자동으로 저장 및 시각화하는 AI 비전 시스템입니다.

---

## 🧪 1. 프로젝트 클론

### 1.1 Git 설치

**Windows**:  
Git 공식 사이트에서 설치

**Mac/Linux**:

```bash
sudo apt install git    # Ubuntu
brew install git        # Mac
```

### 1.2 GitHub에서 프로젝트 클론

```bash
git clone https://github.com/yourusername/smoking-detection-system.git
cd smoking-detection-system
```

---

## 📦 2. 라이브러리 설치

### 2.1 가상환경 설정 (선택사항)

```bash
# 가상환경 생성 (Windows)
python -m venv venv

# 가상환경 활성화
venv\Scripts\activate        # Windows
source venv/bin/activate      # Mac/Linux
```

### 2.2 필요 라이브러리 설치

```bash
pip install -r requirements.txt
```

---

## 🧠 3. YOLOv5 모델 다운로드

### 3.1 모델 파일 준비

- 이미 `best.pt` 모델이 있다면 `/models` 폴더에 복사  
- 필요 시 [YOLOv5 GitHub](https://github.com/ultralytics/yolov5)에서 다운로드 가능

---

## 🎥 4. 웹캠 설정

### 4.1 연결 확인

- Windows: 장치 관리자에서 웹캠 확인  
- Linux: `lsusb` 명령어로 연결 확인

### 4.2 브라우저 접근 허용

- 브라우저에서 카메라 접근 허용 팝업을 수락해야 스트리밍 가능

---

## 🚀 5. 서버 실행

### 5.1 Flask 서버 실행

```bash
python app.py
```

웹 브라우저에서 [http://127.0.0.1:5000](http://127.0.0.1:5000) 접속

---

## 📸 6. 흡연 감지 및 통계

### 6.1 감지 기능

- 실시간 스트리밍 중 흡연자 감지 시 "Stop Smoking Please." 문구 표시  
- 감지된 이미지 `/smoker` 폴더에 자동 저장

### 6.2 통계 시각화

- 메인 웹페이지에 **흡연 감지 횟수** 및 통계 표시  
- 흡연 발생 시마다 수치 자동 갱신

---

## 🛑 7. 서버 종료

```bash
Ctrl + C  # 서버 종료
```

---

## 🛠 8. 추가 설정 (선택)

- **카메라 인덱스 조정**: `cv2.VideoCapture(0)`의 인덱스 값을 1 또는 2로 변경해보세요
- **YOLOv5 모델 재학습**: 더 나은 성능을 위해 사용자 정의 데이터셋으로 추가 학습 가능

---

## 🗂 프로젝트 폴더 구조

```
/smoking-detection-system
├── app.py
├── requirements.txt
├── /static
│   ├── /images
│   │   └── police_logo.png
│   └── /css
│       └── style.css
├── /templates
│   └── index.html
└── /models
    └── best.pt (YOLO 모델)
```

---

> 본 프로젝트는 금연 구역에서의 비흡연 환경을 조성하기 위해  
> 실시간 비전 기술을 적용한 사회적 가치 기반 AI 응용 프로젝트입니다.
