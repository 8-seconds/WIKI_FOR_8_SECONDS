# Android Naming Convention

안드로이드 작명법을 정리한 문서입니다. ~~뭐 작성 할 때마다 노란 줄 보기 싫잖아요..~~

<br>

### 1. Class file

- 클래스 파일 이름은 **UpperCamelCase(aka 파스칼 케이스(PascalCase))** 로 작성한다.

  **ex) SignInActivity, SiginInFragment, ImageUploaderService, ChangePasswordDialog**

<br>

### 2. Resources file

- 리소스 파일 이름은 **snake_case**로 작성한다.

  **ex) image_logo.png, ic_back.xml, menu_main.xml**

<br>

### 3. Layout file

- 레이아웃 파일 이름 또한 마찬가지로 **snake_case**로 작성한다.

  **ex) activity_main.xml, fragment_login.xml, dialog_change_password.xml**

<br>

### 4. Method

- 메소드 이름은 **lowerCamelCase**로 작성한다.

- "동사"로 시작하는 "동사구" 형태를 사용하되, 동사 원형만을 사용한다.

  **ex) showList, updateContacts**

- 한 단어 내에서는 대소문자 변경 없이 사용한다.

  **ex) InVisible :arrow_forward: Invisible**

- 약어 사전에 있는 단어는 되도록 약어를 사용한다.

  **ex) UserInterface :arrow_forward: UI 또는 Ui**

- 자주 사용하는 동사는 용법에 맞게 사용합니다.
  - **show: Invisible한 것을 Visible하게 바꾸는 동작**
  - **check: 어떤 것을 확인한 후 boolean 또는 값으로 반환하는 동작**
  - **is: 어떤 것인지 확인한 후 boolean으로 반환하는 동작**
  - **has: 어떤것을가지고 있는 확인 후 boolean으로 반환하는 동작**

<br>

### 5. 변수

- 변수 이름 또한 마찬가지로 **lowerCamelCase**로 작성한다.

  **ex) isEnd, viewPagerAdapter**

<br>

## :star: ​Case Naming Convention

### 1. UpperCamelCase(PascalCase)

- 쌍봉낙타 표기법이라고도 한다.
- 전체 이름의 첫 문자를 포함한 각 단어의 첫 문자를 대문자로 표시한다.

<br>

### 2. lowerCamelCase

- 단봉낙타 표기법이라고도 한다.
- 보통 카멜 케이스라고 하면 lower 카멜 케이스를 의미한다.
- 각 단어의 첫 문자를 대문자로 표시하되, 이름의 첫 문자는 소문자로 적는다.

<br>

### 3. 스네이크 케이스(snake_case)

- 각 단어의 사이를 **언더바 _** 로 구분해주는 표기법이다.

<br>

## :star: ​참고 자료

##### https://tadomstudio.tistory.com/24

##### http://guswnsxodlf.github.io/camelcase-pascalcase-snakecase
