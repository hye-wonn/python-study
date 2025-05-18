# 6. 캡슐화 (정보 은닉)

-   외부에서 객체의 내부 데이터에 직접 접근하지 못하게 보호
-   변수명 앞에 '\_\_'를 붙이면 private(비공개) 속성으로 설정

```python
class Student:
    def __init__(self, name, age):
        self.__name = name
        self.__age = age

s = Student("홍길동", 20)
# print(s.__age) → 에러 발생 (외부 접근 불가)
```
