# REACT
새 프로젝트 생성 : npx  create-react-app [프로젝트이름]

## 컴포넌트(함수형 작성)
 ```javascript
    function Name(){ // 함수형 컴포넌트 생성시 첫알파벳은 대문자로 시작한다.
        return <div></div> // <- JSX
    }
 ```


export default Name;  <- Name 이라는 컴포넌트를 만들어 내보내겠다 라는 뜻

## JSX
Javascript 와 HTML의 합성어로 XML사용을 허용하는 JS의 확장문법
JSX를 사용하면 어플리케이션 속도를 높히고 가독성을 높혀 코드작성을 더 쉽고 빠르게 할수있음.

## JSX 규칙
1. 태그를 열면 꼭 닫아줘야한다.  
br , input 태그도 예외 X  
selfclosing 을 사용하여 닫을수 있다.  
2. 두개이상의 태그는 꼭 하나의 태그로 감싸져 있어야 한다. 
    ```javascript
    <>
	    <div>두개이상의</div>
	    <p>태그는 하나의 태그로 감싸져 있어야 한다</p>
	<> // 빈태그로 감싸기가 가능하다.
    ```
    
3. javascript 값을 사용할 때는 {} 를 사용한다.  
4. 스타일을 지정해 줄떄는 객체를 생성해야 한다.  
const style = {backgroundColor : 'balck' , color : '#fff'}  
대쉬(-) 로 구분되는 것은 camelcase표기법으로 작성한다.  
5. class대신  className을 사용한다.
6. 주석처리 {/* 주석내용 */}  

## ReactJS 프로젝트의 디럭터리 구조
* node-modules : package manager을 통해 설치된모듈들이 모여있는 디렉토리
* public : ReactJS 의 HTML 파일과 favicon이 들어있는 디렉토리
* src : 대부분의 코딩이 이뤄지는 디렉토리 reactJS 컴포넌트가 모여있는 곳
* package.json : package manager을 통해 설치된 모듈과 스크립트 명령어 등을 담고있는 json파일



