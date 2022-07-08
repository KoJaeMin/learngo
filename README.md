# Go tutorial

|번호|날짜|TIL|
|---|---|---|
|1|2022.07.05| 1. main package만 compile된다.(main은 오직 compile을 위한 것!!)</br> 2. 함수를 export 하고 싶으면 대문자로 해야한다.(대문자로 하면 public 아니면 private으로 지정)</br> 3. 기본적으로 const와 variable로 나눠져 있으며 type도 지정해 줘야 한다.(typescript와 유사)</br> ```const\|var variable_name type = value```</br> 4. func안에서는 축약형인 ```variable_name := value```로 사용할 수 있다. go가 알아서 type을 지정해 준다.(func밖에서의 전역변수 설정은 3번 형식으로만 변수를 선언 및 값 할당을 할 수 있다.)</br> 5. 함수가 여러가지 값을 반환할 수 있다.(!!매우 특이!!)</br> 6. 축약형은 선언하고 사용하지 않으면 작동이 제한 된다.</br> 7. **Naked Return**이란 return 값을 함수 선언부에 선언하는 것이다. 함수 안에서 return하는 변수를 다시 선언할 수 없다. 함수 마지막에 return은 써 줘야 한다.(return만 써도 작동한다.)</br> 8. **defer**는 return 후에 동작한다(=함수가 끝나고도 동작한다.).|