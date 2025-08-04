---
title: "Kotlin 입문 [0]-(개발환경 세팅)"
description: "Kotlin으로 앱을 만들기 위한 환경 설정 방법을 소개합니다."
date: 2025-08-02
update: 2025-08-04
tags:
  - kotlin
series: "Kotlin 앱 만들기"
---

## 앱 개발 언어 및 프레임워크 선택

앱을 만들고 싶다는 생각이 들었습니다.

어떤 언어와 프레임워크를 사용할지 고민이 많았는데요.

> Kotlin? Swift? Flutter? React Native?

아직 구상 단계이고, 안드로이드에 집중해서 공부하고 싶어 **Kotlin**을 선택했습니다.

언어 선택에 있어 저세상개발자님의 유튜브 영상이 큰 도움이 되었습니다.

[![앱을 만드는 방법 유튜브 썸네일](https://img.youtube.com/vi/IGuDm7AMnw4/0.jpg)](https://www.youtube.com/watch?v=IGuDm7AMnw4&ab_channel=%EC%A0%80%EC%84%B8%EC%83%81%EA%B0%9C%EB%B0%9C%EC%9E%90)

---

## Kotlin 개발 환경 설정

**내 개발환경:** `MacBook Pro 14 M4 😎`

### 1. JDK 설치

```bash
brew install openjdk
```

설치 후 환경 변수에 JDK 경로를 추가합니다.

```bash
echo 'export PATH="/opt/homebrew/opt/openjdk/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

### 2. Android Studio 설치

```bash
brew install --cask android-studio
```

설치가 완료되면 Android Studio를 실행합니다.

### 3. Android Studio로 프로젝트 생성

1. Android Studio 실행
2. "New Project" 클릭
3. "Phone and Tablet" > "Empty Activity" 선택
4. 언어를 **Kotlin**으로 설정
5. 프로젝트 이름과 저장 경로 입력 후 "Finish" 클릭

<img src="isthisend.jpg" alt="예. hello world 찍어보시면 됩니다." width="150" height="150"/>

### 4. Kotlin Hello World 예제

아래는 Kotlin으로 작성한 간단한 Hello World 코드입니다.

```kotlin
fun main() {
  println("Hello, World!")
}
```

Android Studio에서 `MainActivity.kt` 파일의 `onCreate` 함수에 아래 코드를 추가하면 앱 화면에 "Hello, World!"가 출력됩니다.

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
  super.onCreate(savedInstanceState)
  setContentView(R.layout.activity_main)
  println("Hello, World!")
}
```

---

## Kotlin 기본 문법

### 변수 선언

```kotlin
val name: String = "홍길동" // 변경 불가(읽기 전용)
var age: Int = 25         // 변경 가능
```

### 함수 선언

```kotlin
fun greet() {
  println("안녕하세요!")
}

fun add(a: Int, b: Int): Int {
  return a + b
}
```

### 조건문

```kotlin
val score = 85
if (score >= 90) {
  println("A")
} else if (score >= 80) {
  println("B")
} else {
  println("C")
}
```

### 반복문

```kotlin
for (i in 1..5) {
  println(i)
}

var count = 0
while (count < 3) {
  println("count: $count")
  count++
}
```

### 클래스 선언

```kotlin
class Person(val name: String, var age: Int) {
  fun introduce() {
    println("저는 $name, $age살 입니다.")
  }
}

val person = Person("홍길동", 25)
person.introduce()
```

---

<br>
<img src="technologia.png" alt="예. 마음껏 만들어 보시면 됩니다."/>

### 만들어 볼 기능

- 위치 공유 기능
- 가족 간 사진 공유 기능
- 유튜브 다운로드
- 유튜브 플레이리스트
- 버스 시간 알기
- ...