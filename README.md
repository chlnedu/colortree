# 🎨 색깔 입체 사전 (3D Color Dictionary)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=three.js&logoColor=white)

아이들이 직접 주변의 사물을 사진으로 찍어 **나만의 3D 색 입체 트리를 완성해가는 에듀테크 웹 애플리케이션**입니다. 
먼셀의 색 입체(Munsell Color System) 원리를 기반으로 설계되어, 아이들이 놀이를 통해 자연스럽게 색상, 명도, 채도의 개념을 시각적으로 학습할 수 있습니다.

> **💡 기획 의도**
> "색깔은 평면이 아니라 입체 공간에 존재한다"는 것을 직관적으로 알려주기 위해 기획되었습니다. 텅 빈 유리 블록에 현실의 색을 채워 넣는 게이미피케이션(Gamification) 요소를 통해 아이들의 수집 욕구와 탐구력을 자극합니다.

<br>

## ✨ 핵심 기능 (Key Features)

### 📸 1. 카메라 연동 및 현실 색상 수집
* 디바이스 카메라 및 사진첩과 직접 연동하여 주변 사물의 사진을 촬영할 수 있습니다.
* **스마트 색상 추출 알고리즘**: 사진의 정중앙(Center Targeting) 픽셀을 분석하여 색상을 추출하고, 실내 그림자로 인해 색이 탁해지는 현상을 막기 위해 **자동 생기 보정(Auto-Enhance)** 알고리즘을 적용했습니다.

### 🌟 2. 3D 인터랙티브 UI (Three.js)
* **바람개비 형태의 구조**: 명도(중심축)를 기준으로 채도가 바깥으로 뻗어나가는 구조를 3D로 완벽하게 구현했습니다.
* **상호작용**: 3D 공간을 스와이프하여 360도로 돌려볼 수 있으며, 칩을 클릭하여 상세 정보를 확인하거나 빈 칩을 클릭해 목표 색상(Target Color) 힌트를 얻을 수 있습니다.
* **성장 애니메이션**: 색상을 획득하면 작은 씨앗 블록이 빛나며 팝핑(Popping)되는 시각적 쾌감을 제공합니다.

### 💾 3. 오프라인 진행도 저장 (Local Storage)
* 별도의 백엔드 서버 없이 브라우저의 `LocalStorage`를 활용해 기기에 아이들의 학습 진행 상황과 사진을 안전하게 저장합니다.
* 앱을 종료했다가 다음 날 다시 켜도 내가 모은 색깔 트리가 그대로 유지됩니다.

<br>

## 🖥 화면 미리보기 (Screenshots)

*(여기에 앱 실행 화면이나 아이패드에서 구동되는 캡처 이미지를 넣어주세요)*

| 기본 화면 (빈 도감) | 목표 색상 힌트 팝업 | 색상 채우기 성공 |
| :---: | :---: | :---: |
| `<img src="이미지링크1" width="250">` | `<img src="이미지링크2" width="250">` | `<img src="이미지링크3" width="250">` |

<br>

## 🛠 기술 스택 및 구조 (Tech Stack)

* **Frontend**: HTML5, CSS3, Vanilla JavaScript (ES6+)
* **3D Rendering**: [Three.js](https://threejs.org/) (r128), OrbitControls
* **Font**: Pretendard (프리텐다드)
* **Architecture**: 
  * `index.html` 단일 파일로 구성된 경량화된 SPA 구조.
  * Canvas API를 활용한 클라이언트 사이드 이미지 리사이징 및 픽셀 데이터 연산(RGB to HSL).

<br>

## 🚀 실행 방법 (How to Run)

본 프로젝트는 순수 프론트엔드 환경으로 구축되어 있어 별도의 서버 설치가 필요하지 않습니다.

1. 이 레포지토리를 클론(Clone)하거나 다운로드합니다.
2. `index.html` 파일을 크롬(Chrome), 사파리(Safari) 등 웹 브라우저로 엽니다.
3. (추천) **GitHub Pages**를 통해 레포지토리를 배포하면 아이패드 등 모바일 기기에서 링크만으로 즉시 접속하여 카메라 기능을 100% 활용할 수 있습니다.
