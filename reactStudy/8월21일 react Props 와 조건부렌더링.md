## props : properties
컴포넌트에서 사용할 데이터 중 변하지 않는 데이터  
부모컴포넌트에서 자식컴포넌트로 데이터를 전달할때 사용  
props의 형태는 string, array, object, function 등 어떤 타입이든 상관없음

### defaultProps
props의 값을 지정해 주지 않았을 경우 default 값으로 지정해 준 값을 사용함

```javascript
    Info.defaultProps = {
        name : '이름이 입력되지 않았습니다.'
    }
```  
위와 같이 Info라는 컴포넌트가 정보를 전달할때 만약 이름 값이 없을경우 이름은 '이름이 입력되지 않았습니다.'라는 값을 가지게 될 것이다.

### props children

## 조건부 렌더링
특정 조건에서 결과에 따라서 다른요소를 보여줌  
렌더링 할때 0 이아닌 false 값 ex) null undefined false 는 렌더링 되지 않는다.
만약 이름만 설정해주고 값으로 블리언 값이 들어갈때 값이 입력되지 않았을 경우 그 값은 true가 된다.
