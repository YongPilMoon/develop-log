---
sidebar_position: 1
---

# 12월

## React Clean Code

#### 응집도: 관련된 일을 하는 코드는 한 곳에 모아서 관리 하자
- 좋은 코드는 != 짧은 코드
- 읽기 좋은 코드가 좋은 코드다

#### 단일책임 원칙 : 한 함수에서 한 가지 일만 하게 하자
- 리엑트 컴포넌트로 기능 불리 가능
```jsx
<LogClick message="제출 버튼 클릭">
    <button onClick={openConfirm}/>
</LogClick>

const LockClick = ({message, children}) => {
    const sendMessage = () => {
       send('message');
    }
    <div onClick={sendMessage}>{children}<div/>
}
```

#### 추상화: 핵심 코드만 남겨 놓고 숨긴
ex) 모달을 연다는 부분을 부모 컴포넌트가 알아야 하나?
추상화 수준이 섞여 있으면 코드 파악이 어렵다.

#### 선언적 프로그래밍 
디테일한 로직은 감추고 중요한 요소는 전달한다
```javascript
<Popup
    onSubmit={회원가입}
    onSuccess={프로필로이동}
/>
```

#### 명령형 프로그래밍
선억적으로 뭉쳐 놓지 않고 하나하나 작성

https://toss.im/slash-21/sessions/3-1

## React에서 비동기를 우아하게 처리하는 법
https://toss.im/slash-21/sessions/3-1

## 실행컨텍스트를 통해 알아보는 호이스팅, 클로져, 스코프 체이닝

### 호이스팅이란?
var로 선언된 변수 혹은 함수가 선언전에 참조되는 현상

```typescript
console.log('hosting: ', hosting)
function1();
var hosting = 123;

function function1 () {
    console.log('function1 is called')
}

// hosting: undefined
// function1 is called
```
자바스크립트에서 변수는 `선언`, `초기화`, `할당` 단계를 거치는데 `var로 선언된 변수`는 선언과 동시에 초기화가 이루어 진다.
그렇기 때문에 코드 실행 단계에서 코드상 아래에 위치한 변수라도 초기화가 되어있고 참조를 해도 에러가 발생하지 않는다. 반면 const, let으로 선언된 변수 들은 코드 실행 단계에 초기화가 되어있지 않고 참조를 하려고 하면 에러가 발생한다.
이 단계를 TDZ(Temporary Dead Zone)이라고 한다.
https://www.youtube.com/watch?v=EWfujNzSUmw