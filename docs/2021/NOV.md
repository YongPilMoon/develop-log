---
sidebar_position: 1
---

# 11월

## Event Loop

- Memory Heap: 변수, 함수가 저장되는 곳
- CallStack: 함수의 실행 컨텍스트가 쌓이는 곳
- EventLoop: CallStack이 비워있을 때 Callback Queue에 쌓인 콜백 함수를 CallStack으로 옮긴다.
- Task Queue: 콜백함수를 쌓아놓는 곳
- WebApi: 비동기 처리 후 Callback Queue에 함수 전달


```typescript
const eventLoop = () => {
  if(checkCallStatck === empty) {
    moveCallbackFunctionToCallStack()
  }
  eventLoop();
}
```
https://www.youtube.com/watch?v=wcxWlyps4Vg
