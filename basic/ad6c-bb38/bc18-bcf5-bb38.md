# 반복문

반복문은 코드를 반복해서 실행할때 사용해야될대 사용되는 구문입니다. 대표적인 반복문으로 while문과 for-in문이 있습니다.

* ### if-else 문법

  if-esle문은 조건에 따라서 코드를 선택하는 선택 구문입니다. 조건은 최종 연산값이 bool값으로 나타나며 조건이 참일경우 if문 구현부가, 거짓일경우 else문 구현부가 선택적으로 실행됩니다.

* ```swift
  if 조건
  {
    //조건이 참일때 실행
  }else
  {
    //조건이 거짓일때 실행
  }
  ```

  한개 이상의 조건이 필요할 경우 조건을 추가 할수 있습니다.  상단의 조건부터 확인하며, 모든 조건이 만족하지 않을때 else문이 실행됩니다.

  ```swift
  if 조건1
  {
    //조건1이 참일때 실행
  }else if 조건2
  {//조건1이 참이 아닐때 확인

    //조건2가 참일때 실행
  }else 
  {
    //모든 조건이 거짓일때 실행
  }
  ```

  조건문은 실행구문으로서 함수 구현부 내에서만 사용이 가능합니다.

  ```swift
  func testFunction()
  {
      if 조건
      {
          //else문 없이 조건문만 독립적으로 사용 가능
      }
  }
  ```

* ### 조건 조합

  조건은 논리연산자와 함께 복합적인 조건으로 조합할수 있습니다.

  ```swift
  func testFunction()
  {
      if 조건1 && 조건2
      {
          //조건 1과 조건2가 모두 참일 경우 실행
      }else if 조건1 || 조건2
      {
          //조건 1과 조건 2 둘중 한개라도 참인 경우 실행
      }else
      {
          //두 조건 모두 거짓일때 실행
      }
  }
  ```

* ### if - else문 예제

  ```
  //짝수 체크
  func isEven(number num:Int) -> Bool
  {
      //파라미터넘버(num)를 2로 나눈 나머지가 0이라면?
      if num % 2 == 0
      {
          return true
      }else
      {
          return false
      }
  }

  //학점 변환
  func grade(for score:Int) -> String
  {    
      var grade:String = "F"
      if score <= 100 && score >= 95
      {
          grade = "A+"
      }else if score >= 90
      {
          grade = "A"
      }else if score >= 85
      {
          grade = "B+"
      }

      return grade

  }
  ```
* ### switch-case

  스위치케이스 문은 값매칭문으로 가장 먼저 매칭되는 case의 값에 구문이 실행됩니다. 위에서부터 매칭을 확인하며 모든 case에 매칭되는 값이 없다면 default문이 실행됩니다. case의 구문의 내용이 없으면 컴파일 에러가 나타납니다.

  ```swift
  switch value
  {
  case value1:
  //value == value1 매칭되면 해당 구문 실행
  print("매칭")
  case value2:
              //아무런 내용이 없으면 컴파일 에러
  default :
  //모든 케이스가 매칭되지 않을때
  print("매칭되는 값 없음")
  }
  ```

  각 case 상태 끝에 콜론\(:\)으로 매칭되는 상태값을 타나내며 콤마\( , \)를 통해 상태를 추가 할 수 있습니다.

  ```swift
  switch num
  {
  case 1,2,3,4,5:
  print("1~5사이값")
  case 6,7,8,9,10:
  print("6~10")
  default:
  print("나머지 정수")
  }
  ```

  switch - case문 역시 실행구문이기 때문에 함수내에서 실행해야만 합니다.

  ```swift
  func sampleSwitch(someCharacter:Character)
  {
      switch someCharacter {
      case "a":
          print("The first letter of the alphabet")
      case "z":
          print("The last letter of the alphabet")
      default:
          print("Some other character")
      }
  }
  ```

* ### swift 매칭

  ㅇㅇㅇ변수를 사용할때는 변수이름을 호출하여 사용할 수 있습니다.

  ```swift
  var number1: Int = 100
  var number2: Int = number1 // 여기에서 number1는 변수의 사용이며 현재 들어 있는 값(100)으로 여겨진다.
  ```

  변수의 값을 사용하여 연산도 가능한데요

  ```swift
  var number1: Int = 100
  var number2: Int = number1 
  var sum: Int = number1 + number2 //sum의 값은 몇 일까요??
  ```

* ### 예제

  다양한 예제를 통해서 변수를 확인해보도록 하겠습니다.

  한번 따라 쳐 보는것도 좋을듯 합니다!

  ```swift
  var myName: String = "WingMan" //선언 + 문자열 값 할당
  myName = "내 이름은 WingMan입니다." //값 재설정

  let userID: String = "wingman" // 상수 선언 및 값 할당, 변경 불가능 
  let age = 20 // 타입 추론을 통한 값 할당

  ////////////
  var biggerNum: Double = 40.5
  var smallNum: Double = 80.2

  var tempNum:Double = biggerNum
  biggerNum = smallNum
  smallNum = tempNum

  ////////////////
  let koreanScore: Int = 100
  let englishScore: Int = 80
  var totalScore = koreanScore + englishScore //변수 값 사용 후 연산
  ```

### 


