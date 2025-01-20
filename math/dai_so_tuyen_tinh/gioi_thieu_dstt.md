# 1. Scalar và Vector

## Vector

Vector là một đại lượng có độ lớn/kích thước (size) và có hướng (direction).

Ví dụ:
- Vận tốc (50 km/h về hướng Bắc), lực (10N về phía Đông).

**Thành phần của vector:**
- **Độ lớn (Magnitude):** Biểu diễn độ mạnh/yếu của vector.
- **Hướng (Direction):** Biểu diễn phương và chiều của vector.

Vector thường biểu diễn các điểm dữ liệu hoặc các đặc trưng (features) trong mô hình.
Ví dụ: một ảnh có thể được biểu diễn dưới dạng vector với mỗi giá trị là cường độ pixel.

## Scalar

Scalar là đại lượng chỉ có độ lớn/kích thước (size), không có hướng.

Ví dụ:
- Nhiệt độ (30°C), khối lượng (5kg), thời gian (10 giây).

Scalar được biểu diễn bằng số thực hoặc số nguyên và thường được sử dụng làm trọng số, bias, hoặc đầu ra của mô hình.

# 2. Biểu diễn Vector trong không gian

## 2.1. Không gian 2D
- Một vector trong 2D có dạng `v = [v_x, v_y]`, với `v_x` và `v_y` là tọa độ theo trục x và trục y.
- **Ví dụ:** `v = [3, 4]` là một vector với độ lớn 5 (công thức tính độ lớn vector chắc mình cũng không cần nhắc lại :))) ) và hướng được xác định bởi `v_x = 3`, `v_y = 4`.

## 2.2. Không gian 3D
- Một vector trong 3D có dạng `v = [v_x, v_y, v_z]`, với `v_z` là tọa độ theo trục z.
- **Ví dụ:** `v = [1, 2, 3]` là một vector trong không gian 3 chiều.

## 2.3. Biểu diễn vector bằng numpy
```python
import numpy as np

# Vector 2D
v_2d = np.array([3, 4])
print("Vector 2D:", v_2d)

# Vector 3D
v_3d = np.array([1, 2, 3])
print("Vector 3D:", v_3d)
```

# 3. Ma trận

## 3.1. Ma trận là gì

- **Định nghĩa:** Ma trận là một bảng chữ nhật chứa các số sắp xếp thành các hàng và cột. Các số này được gọi là phần tử của ma trận.
- **Ký hiệu:** Một ma trận `𝐴` kích thước `𝑚×𝑛` (m hàng, n cột) được viết.

### Cách biểu diễn ma trận
1. Ma trận 2x2
2. Ma trận 3x3
3. Ma trận dạng thưa (sparse matrix)

## 3.2. Mô tả trong Python với numpy
```python
import numpy as np

# Ma trận 2x2
A = np.array([[1, 2], [3, 4]])
print("Ma trận 2x2:")
print(A)

# Ma trận 3x3
B = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print("\nMa trận 3x3:")
print(B)

# Ma trận dạng thưa
C = np.array([[1, 0, 0], [0, 5, 0], [0, 0, 9]])
print("\nMa trận dạng thưa:")
print(C)
```

# 5. Bài tập

## Tạo và in vector, ma trận bằng NumPy

### Yêu cầu bài tập:

#### Tạo vector:
1. Tạo một vector 1 chiều chứa các số nguyên.
2. Tạo một vector 1 chiều chứa các số thực.

#### Tạo ma trận:
1. Tạo một ma trận 2x2 với các số nguyên.
2. Tạo một ma trận 3x3 với các số thực.

#### Thực hành nâng cao:
1. Tạo một ma trận 3x3 dạng thưa (sparse matrix), trong đó hầu hết các phần tử bằng 0.
2. Tạo một ma trận ngẫu nhiên (random matrix) có kích thước 2x3.

### In kết quả:
Hiển thị từng vector và ma trận ra màn hình theo thứ tự.
