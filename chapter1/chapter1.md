# 다트 입문하기

## 1.3 기초 문법

### 메인 함수

```dart
// void는 아무런 값도 반환하지 않는다는 뜻이다.
void main() {

}
```

### 변수 선언

```dart
// 자동 타입 추론. 처음 변수의 값이 String이라면 String으로만
// 변경이 가능하다.
var

// 변수 타입이 고정되지 않음. ts의 any와 비슷하다.
dynamic

String
int
double // 실수
bool // 불린
```

## 1.4 컬렉션

### List

```dart
// js의 Array와 비슷하다. 뒤의 <>는 ts의 타입지정과 비슷하다.
List<String> names = ['Kim', 'Lee', 'Park', 'Choi', 'Jeong'];

add() // js의 push()와 비슷하다.
where() // js의 filter()와 비슷하다.
map() // js의 map()과 비슷하다.
reduce() // js의 reduce()와 비슷하다.

// reduce()와 비슷하지만 fold는 reduce()와
// 달리 어떤 값이든 반환이 가능하다.
fold()
```

### Map

```dart
// js의 Object와 비슷하다.
Map<String, String> dictionary = {
  'Kim': '김',
  'Lee': '이',
  'Park': '박',
  ...적기 귀찮아
}

print(dictionary.keys) // (Kim, Lee, Park)
print(dictionary.value) // (김, 이, 박)
```

### Set

```dart
// 역시 js의 Set과 비슷하다. 중복을 제거한다.
Set<String> name = ['Kim', 'Park', 'Kim'] // ['Kim', 'Park']

// .toList()하면 List로 변환한다.
name.toList();

// Set.from({들어갈 배열})하면 Set과 같이 동작한다.
Set.from(name);
```

## 1.5 연산자

### null 관련 연산자

```dart
int? namber; // null 자동 지정

number ??= 3; // 기존 값이 null일때만 저장
number ??= 4; // 기존 값이 null이 아닌 3이므로 저장되지 않음
```

### 타입 비교 연산자

```dart
// 타입 비교 시 is 사용(= 사용시 에러)

int number = 4;

print(number is int) // true
print(number is double) // false
```
