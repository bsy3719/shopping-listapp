# 쇼핑 리스트 앱

단일 HTML 파일로 만든 한국어 쇼핑 리스트 웹 애플리케이션입니다.

## 실행 방법

별도의 설치나 빌드 과정 없이 `shopping-list.html` 파일을 브라우저에서 바로 열면 됩니다.

```bash
xdg-open shopping-list.html
```

또는 로컬 서버로 실행:

```bash
python3 -m http.server 8000
```

## 기능

- 아이템 추가 (버튼 클릭 또는 Enter 키)
- 체크박스로 완료 처리 (취소선 표시)
- 개별 아이템 삭제
- 완료된 항목 일괄 삭제
- 전체/완료 개수 표시
- localStorage를 통한 데이터 자동 저장 (브라우저 새로고침 후에도 유지)

## 기술 스택

- HTML / CSS / JavaScript (순수 바닐라, 외부 라이브러리 없음)
- localStorage (데이터 영속성)
- Flexbox 레이아웃
