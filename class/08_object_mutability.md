# 8. 객체 전달 및 변경 방법

-   함수로 객체를 전달하면, mutable 객체는 내부에서 변경 가능

```python
class User:
    def __init__(self, name):
        self.name = name

def update_username(u):
    u.name = "변경됨"

user1 = User("원래이름")
update_username(user1)

print(user1.name)
```
