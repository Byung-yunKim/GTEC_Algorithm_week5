# GTEC_Algorithm_week5

```
class Node():
    def __init__(self):
        self.data = None
        self.link = None

node1 = Node()
node1.data = "선모"

node2 = Node()
node2.data = "재서"
node1.link = node2


node3 = Node()
node3.data = "명현"
node2.link = node3

node4 = Node()
node4.data = "아무개"
node3.link = node4

node5 = Node()
node5.data = "김씨"
node4.link = node5

print(node1.data, end = ' ')
print(node1.link.data, end = ' ')
print(node1.link.link.data, end = ' ')
print(node1.link.link.link.data, end = ' ')
print(node1.link.link.link.link.data, end = ' ')

dataArray = ["박1", "박2", "박3", "박4", "박5"]
node = Node()
node.data = dataArray[0]
head = node

for data in dataArray[1:]:
    pre = node
    node = Node()
    node.data = data
    pre.link = node

print(head.data, end = ' ')
print(head.link.data, end = ' ')
print(head.link.link.data, end = ' ')
print(head.link.link.link.data, end = ' ')
print(head.link.link.link.link.data, end = ' ')

node = Node()

node.link = head
node.data = "first"
head = node

print(head.data, end = ' ')
print(head.link.data, end = ' ')
print(head.link.link.data, end = ' ')
print(head.link.link.link.data, end = ' ')
print(head.link.link.link.link.data, end = ' ')

# 1. pre, current 지정
# 2. 노드 검색
# 3. 새 노드 생성
# 4. 새 노드.link를 current 노드로 지정
# 5. pre노드의 link를 새 노드로 지정
# 시험에 나옴

pre = head
current = head.link

while current.link != None:
    if current.data == "박3":
        node = Node()
        node.link = current
        node.data = "2.5"
        pre.link = node
        break
    
    pre = current
    current = current.link

print(head.data, end = ' ')
print(head.link.data, end = ' ')
print(head.link.link.data, end = ' ')
print(head.link.link.link.data, end = ' ')
print(head.link.link.link.link.data, end = ' ')

pre = head
current = head.link

while current.link != None:
    pre = current
    current = current.link

node = Node()
node.data = "end"
current.link = node

print(head.data, end = ' ')
print(head.link.data, end = ' ')
print(head.link.link.data, end = ' ')
print(head.link.link.link.data, end = ' ')
print(head.link.link.link.link.data, end = ' ')
print(head.link.link.link.link.link.data, end = ' ')
print(head.link.link.link.link.link.link.data, end = ' ')
print(head.link.link.link.link.link.link.link.data, end = ' ')

# head 노드 삭제
current = head
head = head.link    # head = current.link
del(current)

print(head.data, end = ' ')
print(head.link.data, end = ' ')
print(head.link.link.data, end = ' ')
print(head.link.link.link.data, end = ' ')
print(head.link.link.link.link.data, end = ' ')
print(head.link.link.link.link.link.data, end = ' ')
print(head.link.link.link.link.link.link.data, end = ' ')

# 특정 노드 삭제
current = head
while current.link != None:
    pre = current
    current = current.link
    
    if current.data == "2.5":
        pre.link = current.link
        del(current)
        break

print(head.data, end = ' ')
print(head.link.data, end = ' ')
print(head.link.link.data, end = ' ')
print(head.link.link.link.data, end = ' ')
print(head.link.link.link.link.data, end = ' ')
print(head.link.link.link.link.link.data, end = ' ')
```
