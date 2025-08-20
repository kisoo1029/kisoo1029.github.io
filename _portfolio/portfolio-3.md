---
title: "웹 기반 To-Do List 애플리케이션"
excerpt: "JavaScript와 Local Storage를 활용한 할 일 관리 웹 앱<br/><img src='/images/500x300.png'>"
collection: portfolio
---

## 프로젝트 개요

순수 JavaScript를 활용하여 구현한 To-Do List 웹 애플리케이션입니다. Local Storage를 활용해 브라우저를 닫아도 데이터가 유지됩니다.

### 핵심 기능

- **CRUD 기능**: 할 일 생성, 읽기, 수정, 삭제
- **데이터 영속성**: Local Storage를 활용한 데이터 저장
- **필터링**: 완료/미완료 항목 필터링
- **드래그 앤 드롭**: 할 일 순서 변경
- **반응형 UI**: 모바일 친화적 인터페이스

### 기술 스택

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **데이터 저장**: Local Storage API
- **스타일링**: Flexbox, Grid Layout
- **아이콘**: Font Awesome

### 주요 학습 내용

1. **DOM 조작**: JavaScript를 통한 동적 UI 업데이트
2. **이벤트 처리**: 사용자 인터랙션 관리
3. **데이터 관리**: JSON 형식의 데이터 저장 및 파싱
4. **ES6 문법**: Arrow functions, Template literals, Destructuring

### 코드 하이라이트

```javascript
// Local Storage에 데이터 저장
function saveTodos() {
    localStorage.setItem('todos', JSON.stringify(todos));
}

// 할 일 추가 함수
function addTodo(text) {
    const todo = {
        id: Date.now(),
        text: text,
        completed: false
    };
    todos.push(todo);
    saveTodos();
    renderTodos();
}
```

### 개선 사항

- 카테고리 기능 추가
- 마감일 설정 기능
- 알림 기능 구현
- 백엔드 연동 (Node.js + MongoDB)
- PWA로 전환하여 오프라인 지원

### 데모

프로젝트의 실제 동작을 확인하실 수 있습니다. 깔끔한 UI와 직관적인 사용성을 목표로 개발했습니다.