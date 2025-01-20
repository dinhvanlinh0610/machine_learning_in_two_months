# Các phép tính với ma trận

## 1. Cộng trừ

### 1.1. Cộng
Phép cộng ma trận chỉ thực hiện khi hai ma trận có cùng kích thước. Nghĩa là số hàng và số cột của hai ma trận phải giống nhau.

**Ví dụ:**
```python
import numpy as np

A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

print(A + B)
```

**Kết quả:**
```
[[ 6,  8],
 [10, 12]]
```

![image](https://github.com/user-attachments/assets/bd1f1399-21f7-4215-b11c-724b8de830bd)

### 1.2. Trừ
Phép trừ ma trận cũng tương tự như phép cộng, nhưng thay vì cộng, ta sẽ trừ từng phần tử của ma trận này với phần tử tương ứng của ma trận kia.

**Ví dụ:**
```python
print(A - B)
```

**Kết quả:**
```
[[-4, -4],
 [-4, -4]]
```

![image](https://github.com/user-attachments/assets/17b9ddd1-bd6e-4637-af4f-2bd6d6194c43)

## 2. Nhân
Nhân ma trận được thực hiện khi số cột của ma trận đầu tiên bằng số hàng của ma trận thứ hai.

![image](https://github.com/user-attachments/assets/504c464a-4228-4284-818f-be02523e2f0f)

```python
E = np.dot(A, B)
print(E)
```

**Kết quả:**
```
[[19 22]
 [43 50]]
```

## 4. Tích Hadamard
Tích Hadamard là phép nhân từng phần tử của hai ma trận cùng kích thước.

![image](https://github.com/user-attachments/assets/286fe277-0b79-4a9e-b69e-a731d705a332)

```python
F = A * B
print(F)  # [[ 5 12]
          #  [21 32]]
```

## 5. Bài tập thực hành
### Bài tập thực hành:

- Tạo ma trận A và B với kích thước 3x3, thực hiện các phép cộng, trừ, và nhân.
- Thực hiện tích Hadamard với hai ma trận đó.
