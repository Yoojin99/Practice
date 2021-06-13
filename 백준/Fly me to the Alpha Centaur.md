```python
test_num = int(input())

def check(distance):
    start_speed = 1
    total_length = 0

    while True:
        total_length = int((start_speed * (start_speed + 1)))
        if total_length > distance:
            break
        start_speed += 1

    start_speed -= 1
    count = start_speed * 2

    if distance != int((start_speed * (start_speed + 1))):
        left = distance - int((start_speed * (start_speed + 1)))
        if left > start_speed + 1:
            count += 1
        count += 1

    print(count)


for _ in range(test_num):
    string = input()
    nums = string.split()

    start = int(nums[0])
    dest = int(nums[1])

    check(dest - start)
```
