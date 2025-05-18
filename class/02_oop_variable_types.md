# 2. 인스턴스 변수와 클래스 변수

## 2-1. 인스턴스 변수

-   객체마다 별도로 존재하는 변수
-   `self.변수명`으로 정의
-   `__init__` 또는 메서드 내부에서 선언

## 2-2. 클래스 변수

-   클래스에 소속된 변수로 모든 인스턴스가 공유함
-   `클래스명.변수명` 또는 `self.__class__.변수명`으로 정의
-   클래스 내부 또는 메서드 밖에서 선언

## 2-3. 인스턴스 / 클래스 변수 예제

```python
class Dog:
    species = "포유류"   # 클래스 변수

    def __init__(self, name):
        self.name = name   # 인스턴스 변수

d1 = Dog("초코")
d2 = Dog("하늘")

print(f"{d1.name}은(는) {d1.species}입니다.")
print(f"{d2.name}은(는) {d2.species}입니다.")
```

## 2-4. 클래스 변수 수정 시 주의점

-   `객체.클래스변수 = 값`
-   해당 인스턴스의 전용 변수가 생성됨 (클래스 변수는 그대로)

```python
d1.species = "조류"
print(d1.species)     # 조류
print(d2.species)     # 포유류 ← 영향 X
```

-   `클래스명.클래스변수 = 값`
-   전체 공유값 변경 방법

```python
Dog.species = "포유류"   # 갱신됨
```
