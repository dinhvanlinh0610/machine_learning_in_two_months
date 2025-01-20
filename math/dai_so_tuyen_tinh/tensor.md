# Tensor: Khái niệm và các thao tác cơ bản

## 1. Khái niệm Tensor

### Lý thuyết
Tensor là một khái niệm tổng quát trong toán học và khoa học máy tính. Tensors là sự mở rộng của khái niệm:
- **Scalar (vô hướng):** Là số vô hướng, không có hướng (ví dụ: `5`).
- **Vector:** Là mảng 1 chiều có hướng (ví dụ: `[1, 2, 3]`).
- **Matrix (ma trận):** Là mảng 2 chiều (ví dụ: `[[1, 2], [3, 4]]`).
- **Tensor:** Là mảng đa chiều (n chiều).

Tensors có thể được sử dụng để biểu diễn dữ liệu dưới nhiều dạng:
- **1D Tensor (Vector):** `[a, b, c]`
- **2D Tensor (Matrix):** `[[a, b], [c, d]]`
- **3D Tensor:** `[[[a, b], [c, d]], [[e, f], [g, h]]]`
- **ND Tensor (Tổng quát):** `n` chiều.

---

## 2. Các phép toán cơ bản trên Tensor

### Tạo Tensor bằng NumPy
NumPy là một thư viện mạnh mẽ để thao tác với mảng n chiều. Dưới đây là một số cách tạo Tensor:

```python
import numpy as np

# Tạo tensor 1D (vector)
tensor_1d = np.array([1, 2, 3])
print("Tensor 1D:")
print(tensor_1d)

# Tạo tensor 2D (ma trận)
tensor_2d = np.array([[1, 2, 3], [4, 5, 6]])
print("\nTensor 2D:")
print(tensor_2d)

# Tạo tensor 3D
tensor_3d = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])
print("\nTensor 3D:")
print(tensor_3d)
```

### Truy cập phần tử trong Tensor
Tensor sử dụng chỉ số để truy cập từng phần tử. Chỉ số bắt đầu từ `0`.
```python
# Truy cập phần tử
print("Phần tử đầu tiên của tensor_1d:", tensor_1d[0])

# Truy cập hàng 1, cột 2 trong tensor_2d
print("Phần tử hàng 1, cột 2 của tensor_2d:", tensor_2d[0, 1])

# Truy cập phần tử trong tensor 3D
print("Phần tử tại (0, 1, 1) của tensor_3d:", tensor_3d[0, 1, 1])
```

---

### Các phép toán cơ bản
Dưới đây là một số phép toán phổ biến trên Tensor:

#### 1. Cộng và trừ
```python
# Cộng và trừ tensor
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

print("A + B:")
print(A + B)

print("\nA - B:")
print(A - B)
```

#### 2. Nhân Hadamard (phép nhân từng phần tử)
```python
# Nhân Hadamard
print("A * B:")
print(A * B)
```

#### 3. Tích ma trận (Matrix Multiplication)
Sử dụng `np.dot` hoặc toán tử `@` để tính tích ma trận.
```python
# Tích ma trận
print("A @ B:")
print(A @ B)

print("\nnp.dot(A, B):")
print(np.dot(A, B))
```

#### 4. Transpose (Chuyển vị)
```python
# Chuyển vị tensor
print("Chuyển vị của A:")
print(A.T)
```

#### 5. Reshape (Thay đổi kích thước Tensor)
```python
# Thay đổi kích thước
tensor = np.array([1, 2, 3, 4, 5, 6])
reshaped_tensor = tensor.reshape(2, 3)
print("Tensor đã được reshape thành (2, 3):")
print(reshaped_tensor)
```

#### 6. Tính tổng, tích, max, min
```python
# Tổng và tích của phần tử
print("Tổng các phần tử của A:", np.sum(A))
print("Tích các phần tử của A:", np.prod(A))

# Giá trị lớn nhất và nhỏ nhất
print("Max của A:", np.max(A))
print("Min của A:", np.min(A))
```

---

## 3. Bài tập thực hành

1. Tạo một tensor 3D kích thước \(2 \times 3 \times 4\).
2. Tính tổng các phần tử trên mỗi trục (axis).
3. Chuyển đổi tensor thành ma trận 2D.
4. Thực hiện các phép cộng, nhân từng phần tử, và tích ma trận trên 2 tensor 2D.

**Gợi ý:**
```python
# 1. Tạo tensor 3D
tensor_3d = np.random.randint(0, 10, (2, 3, 4))
print("Tensor 3D:")
print(tensor_3d)

# 2. Tính tổng trên mỗi trục
print("\nTổng theo trục 0:")
print(np.sum(tensor_3d, axis=0))

print("\nTổng theo trục 1:")
print(np.sum(tensor_3d, axis=1))

print("\nTổng theo trục 2:")
print(np.sum(tensor_3d, axis=2))

# 3. Chuyển đổi tensor 3D thành ma trận 2D
tensor_2d = tensor_3d.reshape(-1, 4)  # Giữ nguyên 4 cột, gộp các chiều còn lại
print("\nTensor 3D chuyển thành ma trận 2D:")
print(tensor_2d)

# 4. Thực hiện các phép toán
A = np.random.randint(1, 5, (2, 2))
B = np.random.randint(1, 5, (2, 2))
print("\nA:")
print(A)
print("\nB:")
print(B)

print("\nA + B:")
print(A + B)

print("\nA * B (Hadamard):")
print(A * B)

print("\nA @ B (Tích ma trận):")
print(A @ B)
```
