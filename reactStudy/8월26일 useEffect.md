## useEffect 
useEffect를 사용하여 특정값이 업데이트 될때 실행할 함수를 정할 수 있다.  
 useEffect에서 등록한 함수는 특정값이 없데이트 되고 난 직후에 실행  
```javascript
useEffect (()=>{
  //마운트될때
  return()=> {
  //언마운트될때 
  }
 }, []); // []안에는 조회해야 할 상태나 props를 넣음
 ```
 
 []를 deps 라하여 의존되는 갑들을 배열 안에 넣어준다. 의존되는 값이 비어있다면 컴포넌트가 처음 화면에 나타날 때만 실행된다.
 
 <b>return() </b>으로 특정함수를 반환하게 되며는 업데이트 되기 바로 직전에 호출 된다.
 
 마운트 될때 예-  
 props를 state로 변환할때, setTimeout , setInterval 함수를 사용할때 사용  
 언마운트 될때 예-  
 clearInterval , 라이브러리 인스턴스를 제거할때 사용  
 

 
