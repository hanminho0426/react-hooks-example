- <a href="https://rinae.dev/posts/a-complete-guide-to-useeffect-ko">참고사이트</a>

- 컴포넌트 사이에서 상태와 관련된 로직을 재사용하기 어렵다.
  - 컨테이너 방식 말고, 상태와 관련된 로직
- 복잡한 컴포넌트들은 이해하기 어렵다.
- Class는 사람과 기계를 혼동시킨다.
  - 컴파일 단계에서 코드를 최적화하기 어렵게 만든다.
- this.state는 로직에서 레퍼런스를 공유하기 때문에 문제가 발생할 수 있따.

- useState
  - state를 대체 할 수 있다.
- ustEffect
  - 라이프 사이클 훅을 대체 할 수 있다.
    - componentDidMount
    - componentDidUpdate
    - componentWillUnmount

```jsx
function Counter() {
  const [count, setCount] = useState(0);

  useEffet(() => {
    document.title = "You clicked ${count} times";
  });

  function click() {
    setCount(count + 1);
  }

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={click}>Click me</button>
    </div>
  );
}
```

### useReducer

- 다수의 하윗값을 포함하는 복잡한 정적 로직을 만드는 경우
- 다음 state가 이전 state에 의존적인 경우
- Redux를 안다면 쉽게 사용 가능
