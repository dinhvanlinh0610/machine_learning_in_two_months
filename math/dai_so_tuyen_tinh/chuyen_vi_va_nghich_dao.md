# Ma trận chuyển vị và nghịch đảo

## 1. Ma trận chuyển vị

### Lý thuyết
Ma trận chuyển vị của ma trận \( A \) được ký hiệu là \( A^T \). Ma trận chuyển vị được tạo bằng cách hoán đổi hàng thành cột và cột thành hàng.

**Ví dụ:**
Cho ma trận \( A \):
\[
A =
\begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{bmatrix}
\]

Ma trận chuyển vị \( A^T \) là:
\[
A^T =
\begin{bmatrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{bmatrix}
\]

### Sử dụng Python (NumPy)
```python
import numpy as np

A = np.array([[1, 2, 3], [4, 5, 6]])

# Ma trận chuyển vị
A_T = A.T
print(A_T)
```

**Kết quả:**
```
[[1 4]
 [2 5]
 [3 6]]
```

---

## 2. Ma trận nghịch đảo

### Lý thuyết
Ma trận nghịch đảo của ma trận vuông \( A \) (kích thước \( n \times n \)) là ma trận \( A^{-1} \) sao cho:
\[
A \cdot A^{-1} = I
\]
Trong đó \( I \) là ma trận đơn vị.

**Điều kiện tồn tại:**  
Ma trận \( A \) phải là **ma trận vuông** và **định thức khác 0** (\( \text{det}(A) \neq 0 \)).

**Công thức tính tay (cho ma trận \( 2 \times 2 \)):**
Cho ma trận \( A \):
\[
A =
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
\]

Nghịch đảo của \( A \) là:
\[
A^{-1} = \frac{1}{\text{det}(A)} \cdot
\begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}
\]
Với \( \text{det}(A) = ad - bc \).

**Ví dụ:**
Cho \( A = \begin{bmatrix} 4 & 7 \\ 2 & 6 \end{bmatrix} \), ta tính:
\[
\text{det}(A) = (4 \cdot 6) - (7 \cdot 2) = 24 - 14 = 10
\]

Nghịch đảo:
\[
A^{-1} = \frac{1}{10} \cdot
\begin{bmatrix}
6 & -7 \\
-2 & 4
\end{bmatrix}
=
\begin{bmatrix}
0.6 & -0.7 \\
-0.2 & 0.4
\end{bmatrix}
\]

### Sử dụng Python (NumPy)
```python
import numpy as np

A = np.array([[4, 7], [2, 6]])

# Kiểm tra định thức
det = np.linalg.det(A)
print(f"Định thức của A: {det}")

if det != 0:
    # Ma trận nghịch đảo
    A_inv = np.linalg.inv(A)
    print("Ma trận nghịch đảo:")
    print(A_inv)
else:
    print("Ma trận không có nghịch đảo.")
```

**Kết quả:**
```
Định thức của A: 10.0
Ma trận nghịch đảo:
[[ 0.6 -0.7]
 [-0.2  0.4]]
```

---

## 3. Bài tập thực hành

- Tạo một ma trận vuông \( A \) kích thước \( 3 \times 3 \).
- Thực hiện:
  1. Tính ma trận chuyển vị của \( A \).
  2. Kiểm tra xem \( A \) có nghịch đảo không. Nếu có, tính ma trận nghịch đảo của \( A \).
```python
# Gợi ý bài tập
A = np.array([[1, 2, 3], [0, 1, 4], [5, 6, 0]])

# Ma trận chuyển vị
print("Ma trận chuyển vị của A:")
print(A.T)

# Định thức
det = np.linalg.det(A)
print(f"Định thức của A: {det}")

# Ma trận nghịch đảo
if det != 0:
    A_inv = np.linalg.inv(A)
    print("Ma trận nghịch đảo của A:")
    print(A_inv)
else:
    print("Ma trận không có nghịch đảo.")
```
