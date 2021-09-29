---
sidebar_position: 1
---

# 9월

## Mac에서 여러개의 github 계정 사용하기

ssh config 파일을 이용
https://jintaewoo.tistory.com/44

## 브라우저 랜더링 과정과 애니메이션 최적화
dom tree, css tree -> render tree -> layout(reflow) -> paint(repaint) -> composite
뒤로 갈수록 비용이 적음
1. 적은비용으로 변경할 수 있는 속성을 이용하자(left,top(layout) 보다는 translate(composite))
2. layout이 변경이 필요할 경우 최대한 주변 layout 변경에 영향을 미치지 않는 쪽으로 구현하자(ex absolute 혹인 fixed 요소의 left, top)

css 속성별 어떤 변화가 일어나는지 (https://csstriggers.com/) 
https://www.youtube.com/watch?v=4PStxeSIL9I
https://www.youtube.com/watch?v=sJ14cWjrNis&list=PLgXGHBqgT2TvpJ_p9L_yZKPifgdBOzdVH&index=32

## OSI 7계층
https://www.youtube.com/watch?v=1pfTxp25MA8&list=PLgXGHBqgT2TvpJ_p9L_yZKPifgdBOzdVH&index=94
