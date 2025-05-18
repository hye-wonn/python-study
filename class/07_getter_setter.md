# 7. 접근자와 설정자

## 7-1. 접근자 (Getter)

-   private 변수의 값을 가져옴
-   외부 접근 제어 및 유효성 검사 가능

## 7-2. 설정자 (Setter)

-   private 변수의 값을 설정

## 7-3. 접근자 / 생성자 사용 예제

```python
class Student:

    def __init__(self, name, age):
        self.__name = name
        self.__age = age

    def getName(self):
        return self.__name

    def setName(self, name):
        self.__name = name

    def getAge(self):
        return self.__age

    def setAge(self, age):
        self.__age = age

person = Student("이름 없음", 20)
person.setName("혜원")

print(f"학생 이름: {person.getName()}, 학생 나이: {person.getAge()}")
```
