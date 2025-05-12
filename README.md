# ab-testing-conversion-rate-analysis

이 프로젝트는 웹사이트의 **기존 랜딩 페이지(old_page)**와 **새로운 랜딩 페이지(new_page)** 중 어느 쪽이 더 높은 전환율을 가지는지를 분석하기 위한 A/B 테스트 결과를 다룹니다.

## 📊 문제 정의

사용자는 무작위로 다음 두 그룹 중 하나에 배정됩니다:
- **Control 그룹**: 기존 페이지(`old_page`)를 본 사용자
- **Treatment 그룹**: 새로운 페이지(`new_page`)를 본 사용자

가설은 다음과 같습니다:

- **귀무가설(H0)**: `new_page`의 전환율 ≤ `old_page`의 전환율  
- **대립가설(H1)**: `new_page`의 전환율 > `old_page`의 전환율

## 📁 구성 파일

- `notebook/a_b_testing_kaggle.ipynb`: 전체 분석, 시각화, 통계 검정이 담긴 노트북
- `data/ab_data.csv`: 원본 데이터셋 (개인정보/용량 문제로 GitHub에는 업로드하지 않음)
- `requirements.txt`: 사용된 파이썬 라이브러리 목록 (선택 사항)

## 🧪 분석 방법

- 탐색적 데이터 분석(EDA)
- 데이터 정제: 그룹과 페이지 불일치 제거, 중복 사용자 제거
- 전환율 비교 시각화
- 카이제곱 검정, Z-검정
- 전환율 차이의 신뢰구간 계산

## ✅ 결론

통계 검정 결과 p-value가 유의수준(0.05)보다 커서 귀무가설을 기각할 수 없었습니다.  
따라서 **새로운 페이지가 기존 페이지보다 전환율이 높다는 통계적으로 유의미한 근거는 없습니다.**

## 🛠️ 사용 기술

- Python (Pandas, Seaborn, Matplotlib)
- Scipy, Statsmodels
- Jupyter Notebook
