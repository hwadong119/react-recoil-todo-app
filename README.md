## recoil 설치
```terminal
npm install recoil
```

<br><br>

## 사용

리코일을 사용하고자 하는 컴포넌트에 \<RecoilRoot>\</RecoilRoot> 로 감싸줌

<br><br>

## Atom

- Atom은 상태(state)의 일부를 나타냄

- 어떤 컴포넌트에서나 읽고 쓸 수 있음

- atom의 값을 읽는 컴포넌트들은 암묵적으로 atom을 구독함. 그래서 atom에 어떤 변화가 있으면 그 atom을 구독하는 모든 컴포넌트들이 재렌더링 되는 결과가 발생

- useRecoilState()를 사용하여 컴포넌트가 atom을 읽고 쓰게 함 

- useSetRecoilState() 훅을 사용하여 전역 상태의 setter 함수 접근

- useRecoilValue() 훅을 사용하여 전역 상태의 state 상태 값만을 참조

- useResetRecoilState() 훅을 사용하여 전역 상태를 default(초기값)으로 Reset

<br><br>

## Selector

- Selector는 atom 혹은 다른 Selector 상태를 입력받아 동적인 데이터를 반환하는 순수 함수

- Selector가 참조하던 다른 상태가 변경되면 이도 같이 업데이트 되며, 이때 Selector를 바라보던 컴포넌트들이 리렌더링 되는 것

- useRecoilValue() 훅을 사용

<br><br>

## 비동기 데이터 쿼리

Selector를 이용해 비동기 요청을 한 데이터를 전역 상태에 넣어주기

- selector는 기본적으로 값을 자체적으로 캐싱

- 만약 입력된 적이 있는 값이라면 그 값을 기억하고, 이 값이 다시 호출 되면 이전에 캐싱된 결과를 바로 보여주기 때문에 비동기 데이터를 다루는 측면에서 유리

- 유저 데이터 같은 데이터는 애플리케이션을 만들 때 많은 컴포넌트에서 사용되기 때문에 전역 상태로 관리하면 좋음


<br><br>
<br><br>
<br><br>
<br><br>
