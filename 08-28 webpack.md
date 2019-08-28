# webpack

webpack이 없을때 브라우저는 각 기능에 대한 javascript를 로드한다.  
이때 너무 많은 스크립트를 로드하면 네트워크 병목 현상이 일어나게 된다.  
그렇다고 모든 스크립트가 포함되어있는 javascript코드를 만들게 되면 가독성이 떨어지고 크기가 커지며 유지관리가 어렵게 된다.  
이렇기에 webpack는 http 커넥션을 최소화 하고 병목현상을 없에기 위해 js파일을 하나의 bundle파일로 만드는 일을 해준다.

webpack는 4가지 핵심개념이 있다. <b>진입 출력 로더 플러그인</b>

## 진입
entry : 앱의 위치와 번들링 프로세스가 시작되는 지점  
webpack4부터 생략가능 생략시 ./src/index 가 기본으로 설정

##출력 
output : 번들링 프로세스가 끝난후 번들링 된 파일을 저장할 장소와 이름을 정함  
filename : 'bundle.js' 웹팩출력의 표준이름  
path : 경로!! 절때 경로를 사용해야됨  
절때 경로에 접근하려면 노드패키지를 사용해야한다. 
```javascript
    const path = require('path')
```  

## 플러그인
플러그인을 사용하면 복잡한 처리를 수행 할 수있다.
```javascript
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin') 

module.exports = {
    entry : './src/js/index.js',
    output : {
        path : path.resolve(__dirname,'dist'),
        filename : 'js/bundle.js'
    },
    devServer : {
        contentBase : './dist'
    },
    plugins : [
        new HtmlWebpackPlugin({
            filename : 'index.html',
            template : './src/index.html'
        })
    ]
}
```  

위 코드는 HtmlWebpackPlugin 을 사용했다. 이 플러그인은 src폴더에서 쓰여진 html파일을 dist파일에 소스를 보여줄수있다.  
