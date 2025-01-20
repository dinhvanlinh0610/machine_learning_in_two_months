# Norm Vector: Norm L1/L2 (Vector Norms)

## 1. Khái niệm về Norm của Vector

### Lý thuyết
Norm của một vector đo độ dài hoặc độ lớn của vector đó trong không gian. Có nhiều loại norm khác nhau, nhưng phổ biến nhất là:
- **L1 Norm (Manhattan Distance):** Tổng giá trị tuyệt đối của các phần tử trong vector.  
  **Công thức:**  
  `Norm L1 = Tổng các giá trị tuyệt đối của các phần tử trong vector`  
  Ví dụ: Nếu vector v = [3, -4], thì Norm L1 = |3| + |-4| = 3 + 4 = 7.
  
- **L2 Norm (Euclidean Distance):** Căn bậc hai của tổng bình phương các phần tử trong vector.  
  **Công thức:**  
  `Norm L2 = Căn bậc hai của tổng các bình phương các phần tử trong vector`  
  Ví dụ: Nếu vector v = [3, -4], thì Norm L2 = √(3² + (-4)²) = √(9 + 16) = √25 = 5.

Norm thường được sử dụng trong học máy và xử lý tín hiệu để đo độ lớn của vector hoặc chuẩn hóa dữ liệu.

---

## 2. Tính toán Norm bằng tay

Giả sử một vector `v = [3, -4]`:
- **L1 Norm:**
  `Norm L1 = |3| + |-4| = 3 + 4 = 7`
- **L2 Norm:**
  `Norm L2 = √(3² + (-4)²) = √(9 + 16) = √25 = 5`

---

## 3. Tính toán Norm bằng NumPy

Sử dụng thư viện NumPy, bạn có thể tính toán L1 và L2 Norm dễ dàng.

```python
import numpy as np

# Tạo vector
v = np.array([3, -4])

# L1 Norm
l1_norm = np.sum(np.abs(v))
print("L1 Norm:", l1_norm)

# L2 Norm
l2_norm = np.sqrt(np.sum(v**2))
print("L2 Norm:", l2_norm)

# Hoặc sử dụng các hàm NumPy tích hợp
l1_norm_np = np.linalg.norm(v, ord=1)
l2_norm_np = np.linalg.norm(v, ord=2)

print("L1 Norm (NumPy):", l1_norm_np)
print("L2 Norm (NumPy):", l2_norm_np)

```

---

## 4. Chuẩn hóa Vector bằng Norm

Chuẩn hóa vector là quá trình biến đổi vector sao cho norm của nó bằng 1, thường được gọi là **Unit Vector**. 

### Công thức
`v_normalized = v / Norm(v)`

### Ví dụ
Chuẩn hóa vector `v = [3, -4]`:
1. **Tính L2 Norm:** Norm L2 = 5
2. **Chuẩn hóa:** 
   `v_normalized = (1 / 5) * [3, -4] = [0.6, -0.8]`

### Thực hiện với NumPy
```python
# Chuẩn hóa vector
v_normalized = v / np.linalg.norm(v, ord=2)
print("Vector đã được chuẩn hóa:", v_normalized)

## 5. Bài tập thực hành

1. Tính L1 và L2 Norm cho vector `v = [1, -2, 3, -4]`.
2. Chuẩn hóa vector `v` bằng L2 Norm.
3. Tạo một ma trận `A = [[1, 2], [3, 4]]` và tính norm của từng hàng trong ma trận.

**Gợi ý:**
```python
# Bài 1: Tính L1 và L2 Norm
v = np.array([1, -2, 3, -4])
l1_norm = np.linalg.norm(v, ord=1)
l2_norm = np.linalg.norm(v, ord=2)
print("L1 Norm:", l1_norm)
print("L2 Norm:", l2_norm)

# Bài 2: Chuẩn hóa vector
v_normalized = v / np.linalg.norm(v, ord=2)
print("Vector đã được chuẩn hóa:", v_normalized)

# Bài 3: Tính norm của từng hàng trong ma trận
A = np.array([[1, 2], [3, 4]])
row_norms = np.linalg.norm(A, ord=2, axis=1)
print("Norm của từng hàng trong ma trận:")
print(row_norms)
