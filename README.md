# Go tutorial

|번호|날짜|TIL|
|---|---|---|
|1|2022.07.05| 1. main package만 compile된다.(main은 오직 compile을 위한 것!!)</br> 2. 함수를 export 하고 싶으면 대문자로 해야한다.(대문자로 하면 public 아니면 private으로 지정)</br> 3. 기본적으로 const와 variable로 나눠져 있으며 type도 지정해 줘야 한다.(typescript와 유사)</br> ```const\|var variable_name type = value```</br> 4. func안에서는 축약형인 ```variable_name := value```로 사용할 수 있다. go가 알아서 type을 지정해 준다.(func밖에서의 전역변수 설정은 3번 형식으로만 변수를 선언 및 값 할당을 할 수 있다.)</br> 5. 함수가 여러가지 값을 반환할 수 있다.(!!매우 특이!!)</br> 6. 축약형은 선언하고 사용하지 않으면 작동이 제한 된다.</br> 7. **Naked Return**이란 return 값을 함수 선언부에 선언하는 것이다. 함수 안에서 return하는 변수를 다시 선언할 수 없다. 함수 마지막에 return은 써 줘야 한다.(return만 써도 작동한다.)</br> 8. **defer**는 return 후에 동작한다(=함수가 끝나고도 동작한다.).|
|2|2022.07.09| 1. go에서 반복문은 for만 존재한다.(JavaScript와 매우 비슷)</br> 2. range는 index와 value를 같이 return함.(한개만 받을 경우 index만 받을 수 있다.)</br> 3. **if문**작성시 변수를 바로 선언할 수 있다.(variable expression)</br> 4. ```C/C++```과 같이 pointer를 사용 가능하다.(다만 해제는 **가비지 컬렉터**가 해주기에 해제는 할 수 없다.)</br> 5. Go에는 Array와 Slice가 있는 데 각각은 C++에서의 정적배열과 동적배열이라 할 수 있다.</br> 6. Slice는 ```append(slice,value)```라는 함수로 return한 값을 다시 받으면 값이 추가 된다.</br> 7. **map**이라는 key-value 형태의 자료구조가 존재한다.(JavaScript의 object와 비슷하지만 tpye을 정적으로 선언하는 것이 다르다.)</br> 8. Class가 없고 **Struct**만 있다. **Struct**에는 데이터만 넣을 수 있다. 하지만 구조체의 외부에 method를 생성해서 사용할 수 있다.([참고][1])|



[1]: https://golangkorea.github.io/post/go-start/object-oriented/ "Go와 객체지향"
