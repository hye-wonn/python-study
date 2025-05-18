# 5. self

## 5-1. self 정의

-   메서드 내부에서 자기 자신(인스턴스)을 가르킴
-   인스턴스 변수에 접근할 때 필수
-   생략하면 에러가 발생하며, 항상 첫 번째 인자로 사용

```python
class Student:
    def __init__(self, name, age):
        self.name = name   # self.name = 전달받은 name
        self.age = age     # self.age = 전달받은 age

    def introduce(self):
        print(f"제 이름은 {self.name}이고, 나이는 {self.age}살 입니다.")

s = Student("유혜원", 20)
s.introduce()
```

## 5-2. 기본값 설정

-   매개변수에 기본값을 주면 객체 생성 시 생략 가능

```python
class Person:
    def __init__(self, name = "이름 없음", age = 0):
        self.name = name
        self.age = age

p1 = Person()
p2 = Person("혜원", 20)

print(f"이름: {p1.name}, 나이: {p1.age}")
print(f"이름: {p2.name}, 나이: {p2.age}")
```
