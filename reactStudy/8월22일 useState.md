## useState를 통한 동적 상태관리 
Hooks는 react 16.8버전부터 함수형 컴포넌트에서 동적상태를 관리할 수 있게 해준다.  
import React , {useState} from 'react' 를 통해서 호출 할 수있다.  
<b>useState</b>는 두개의 요소가 들어있는 배열을 반환한다.  
[현재상태 , 현재상태를 변경시킬 수 있는 함수]의 형태로 반환  
<br>
```javascript
import React , {useState} from 'react'
import './Counter.css'

function Counter(){
    let [number , setNumber] = useState(0)
    const increase = function(){
        setNumber(number + 1)
    }

    const decrease = function(){
        setNumber(number - 1)
    }

    const reset = function(){
        setNumber(number = 0)
    }
    
    return (
        <div className="wrap">
            <h1>{number}</h1>
            <button onClick={increase}>+1</button>
            <button onClick={decrease}>-1</button>
            <button onClick={reset}>reset</button>
        </div>
    )
}

export default Counter;
```
 useState를 사용한 카운터만들기
