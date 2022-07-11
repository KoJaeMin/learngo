# Go tutorial

|번호|날짜|TIL|
|---|---|---|
|1|2022.07.05| 1. main package만 compile된다.(main은 오직 compile을 위한 것!!)</br> 2. 함수를 export 하고 싶으면 대문자로 해야한다.(대문자로 하면 public 아니면 private으로 지정)</br> 3. 기본적으로 const와 variable로 나눠져 있으며 type도 지정해 줘야 한다.(typescript와 유사)</br> ```const\|var variable_name type = value```</br> 4. func안에서는 축약형인 ```variable_name := value```로 사용할 수 있다. go가 알아서 type을 지정해 준다.(func밖에서의 전역변수 설정은 3번 형식으로만 변수를 선언 및 값 할당을 할 수 있다.)</br> 5. 함수가 여러가지 값을 반환할 수 있다.(!!매우 특이!!)</br> 6. 축약형은 선언하고 사용하지 않으면 작동이 제한 된다.</br> 7. **Naked Return**이란 return 값을 함수 선언부에 선언하는 것이다. 함수 안에서 return하는 변수를 다시 선언할 수 없다. 함수 마지막에 return은 써 줘야 한다.(return만 써도 작동한다.)</br> 8. **defer**는 return 후에 동작한다(=함수가 끝나고도 동작한다.)([참고][8]).|
|2|2022.07.09| 1. Go에서 반복문은 for만 존재한다.(JavaScript와 매우 비슷)</br> 2. range는 index와 value를 같이 return함.(한개만 받을 경우 index만 받을 수 있다.)</br> 3. **if문** 작성시 변수를 바로 선언할 수 있다.(variable expression)</br> 4. ```C/C++```과 같이 pointer를 사용 가능하다.(다만 해제는 **가비지 컬렉터**가 해주기에 해제는 할 수 없다.)([참고][1])</br> 5. Go에는 Array와 Slice가 있는 데 각각은 C++에서의 정적배열과 동적배열이라 할 수 있다.</br> 6. slice는 ```append(slice,value)```라는 함수로 return한 값을 다시 받으면 값이 추가 된다.</br> 7. **map**이라는 key-value 형태의 자료구조가 존재한다.(JavaScript의 object와 비슷하지만 tpye을 정적으로 선언하는 것이 다르다.)</br> 8. Class가 없고 **Struct**만 있다. **Struct**에는 데이터만 넣을 수 있다. 하지만 구조체의 외부에 method를 생성해서 사용할 수 있다.([참고][2])|
|3|2022.07.11| 1. Go는 삼항연산자를 지원하지 않는다.([참고][3])</br> 2. Go에서 export하면 comment를 다는 것을 추천한다. comment다는 방법은 export하는 것 위에 주석을 생성하고 export하는 것의 이름을 작성한 뒤 한 칸을 띄고 작성하면 된다.</br> 3. Go에서 내장 모듈이 아닌 다른 모듈을 사용하기 위헤서는 **모듈 생성**을 하고 사용이 가능하다.([참고][4])</br> 4. **Struct**를 export할 때, ```call-by-value```가 아닌 ```call-by-reference```를 이용해야 값을 변경이 가능하다.([참고1][5], [참고2][6])</br><p align="center"><img src="https://miro.medium.com/max/1000/1*GXoMWqljArmbjB0ReNioag.gif"></p></br> 5. Go에서 method를 만드는 방법은 func과 메서드 이름 사이에 **receiver**를 넣어주어야 한다. 단, **receiver**는 **Struct**의 첫 글자의 소문자로 시작해야한다.</br>ex) ```func (receiver ReceiveStruct) MyMethod()```</br> 6. Go에서는 **Error 처리**를 직접 해줘야 한다. Error는 **error**와 **nil**이라는 값을 가질 수 있다. **nil**은 Error가 나지 않았다는 것을 의미한다.(JavaScript에서의 null/None과 같다.)([참고][7])</br> 7. ```log.Fatalln(myerror)```은 ```myerror```을 ```fmt.Println(myerror)``` 후 process를 종료시킨다.|


[1]: https://taesunny.github.io/programming/go-garbage-collection/ "[Go] Go Garbage Collection"
[2]: https://golangkorea.github.io/post/go-start/object-oriented/ "Go와 객체지향"
[3]: https://blog.advenoh.pe.kr/go/Go-Ternary-Operator-%EC%82%BC%ED%95%AD%EC%97%B0%EC%82%B0%EC%9E%90/ "Go Ternary Operator (삼항연산자)"
[4]: https://www.vompressor.com/go-mod/ "Go 모듈을 사용해보자"
[5]: https://david-yappeter.medium.com/golang-pass-by-value-vs-pass-by-reference-e48aac8b2716 "Golang Pass by value vs Pass by reference"
[6]: https://codewithyury.com/golang-pass-by-pointer-vs-pass-by-value/ "Pass by pointer vs pass by value in Go"
[7]: https://shortstories.gitbook.io/studybook/go/go-error-handling "Go Error handling"
[8]: https://go.dev/blog/defer-panic-and-recover "Defer, Panic, and Recover"