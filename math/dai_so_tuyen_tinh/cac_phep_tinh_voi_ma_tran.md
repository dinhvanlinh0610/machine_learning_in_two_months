Các phép tính với ma trận

1. Cộng trừ
1.1. Cộng
   Phép cộng ma trận chỉ thực hiện khi hai ma trận có cùng kích thước. Nghĩa là só hàng và số cột của 2=hai ma trận phải giống nhau.
   Ví dụ:
   import numpy as np
  A = np.array([[1, 2], [3, 4]])
  B = np.array([[5, 6], [7, 8]])
  print(A + B)

   Kết quả"
   [[ 6,  8],
    [10, 12]]

1.2. Trừ
   Tương tự như phép cộng, phép trừ cũng yêu cầu hai ma trận phải có cùng kích thước.
   Ví dụ:
   print(A - B)
   [[-4, -4],
    [-4, -4]]



3. Nhân
4. Tích hadamard
5. Bài tập thực hành

   
