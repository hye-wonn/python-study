# 3. 메서드

## 3-1. 메서드 정의

-   클래스 내부에서 정의된 함수
-   첫 번째 인자로 `self` 사용

## 3-2. 인스턴스 메서드

-   클래스 내부에서 일반적으로 사용하는 메서드
-   `self` 인자 필수 → 객체의 속성에 접근 가능

```python
class Student:

    def __init__(self, name):
        self.name = name

    def say_hello(self):
        print(f"{self.name}님, 안녕하세요!")

s = Student("혜원")
s.say_hello()
```

## 3-3. 클래스 메서드

-   클래스 자체를 대상으로 하는 메서드
-   cls 인자 필수 → 클래스 변수에 접근 가능
-   클래스 변수(공통 데이터)를 변경할 때 사용

```python
class Student:
    count = 0

    def __init__(self, name):
        self.name = name
        Student.count += 1

    def get_count(cls):
        print(f"현재 학생 수: {cls.count}")

Student("학생1")
Student("학생2")
Student.get_count()
```

## 3-4. 정적 메서드

-   클래스나 객체 정보(self, cls) 없이 실행 가능한 함수
-   일반 함수를 클래스 내부에 넣어두고 싶을 때 사용
-   계산, 검증 등의 유틸리티 함수에 적합

```pyhton
class Math:

    def add(x, y):
        return x + y

print(Math.add(3, 5))
```
