# 4. 생성자

## 4-1. 생성자 정의

-   `__init__` 메서드로 정의
-   객체를 생성할 때 자동으로 실행
-   인스턴스 변수 초기화에 사용

```python
# 생성자 정의 구조
class 클래스명:
    def __init__(self, 매개변수들):
        초기화 코드   # type: ignore
```

## 4-2. 생성자 사용 예제

```python
# 생성자 예제 1
class Counter:
    def __init__(self):
        self.count = 0

a = Counter()   # count = 0 으로 초기화됨

# 생성자 예제 2
class Dog:
    def __init__(self):
        print("강아지가 태어났어요!")

# 객체 생성 시 자동으로 __init__이 호출됨
puppy = Dog()
```
