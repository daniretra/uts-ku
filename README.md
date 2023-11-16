# 1. Persamaan Non Linier
Persamaan non linier yang diberikan adalah:
3 + x³ - x = 4
3 + x³ - x - 4 = 0
x³ - x + 3 - 4 = 0
x³ - x - 1 = 0 atau
x³ - x = 1

# Solusi :

```Python:

def fungsi_non_linier(x):
    return x**3 - x + 3 - 4
	
def turunan_fungsi_non_linier(x):
    return 3*x**2 - 1

def metode_newton_raphson(x0, toleransi, maks_iter):
    iterasi = 1
    while iterasi <= maks_iter:
          x1 = x0 - fungsi_non_linier(x0) / turunan_fungsi_non_linier(x0)
          print(f'Iterasi {iterasi}: x = {x1}')

	  if abs(x1 - x0) < toleransi:
	     print(f'Solusi ditemukan setelah {iterasi} iterasi: x = {x1}')
	     return x1

	     x0 = x1
	     iterasi += 1

	  print('Iterasi maksimum tercapai. Metode Newton-Raphson tidak konvergen.')
	  return None

# a. Tentukan nilai awal, toleransi, dan maksimum iterasi
x0 = 1.0
toleransi = 1e-6
maks_iter = 100

# b. Panggil fungsi untuk metode Newton-Raphson
solusi = metode_newton_raphson(x0, toleransi, maks_iter)
Output:

Iterasi 1: x = 1.5 
Iterasi 2: x = 1.3478260869565217 
Iterasi 3: x = 1.325200398950907 
Iterasi 4: x = 1.3247181739990537 
Iterasi 5: x = 1.3247179572447898 
Solusi ditemukan setelah 5 iterasi: x = 1.3247179572447898 ```
```


# 2. Persamaan Linier
Persamaan linier yang diberikan adalah:
2x - 4 = 8
2x = 8 + 4
2x = 12
x = 6
Jadi, solusi persamaan linier ini adalah x = 6.

# Solusi
Berikut adalah implementasi dalam Python:

```
def solve_linear_equation(coef, constant):
# Persamaan linear: coef * x = constant
x = constant / coef
return x

# Koefisien persamaan
coef = 2

# Konstanta persamaan
constant = 8 + 4  # Sisi kanan persamaan dipindahkan ke sisi kiri dengan menggabungkan konstanta

# Panggil fungsi untuk menyelesaikan persamaan linear
solusi = solve_linear_equation(coef, constant)

# Cetak solusi
print(f"Solusi persamaan 2x - 4 = 8 adalah x = {solusi}")
Output :

Solusi persamaan 2x - 4 = 8 adalah x = 6.0

# 3. nilai x
Mari kita selesaikan kedua persamaan tersebut:

 1. Persamaan non-linier: \(3 + x^3 - x = 4\)

Mari kita gabungkan semua istilah pada satu sisi persamaan:

\[ x^3 - x = 1 \]

Sehingga kita memiliki persamaan kubik:

\[ x^3 - x - 1 = 0 \]

Persamaan ini mungkin memerlukan metode numerik atau grafik untuk mencari akar-akarnya. Dalam kasus ini, kita tidak dapat dengan mudah menemukan solusi eksplisitnya. Anda mungkin perlu menggunakan metode numerik seperti metode Newton atau metode iteratif lainnya untuk mendekati solusi.

 2. Persamaan linier: \(2x - 4 = 8\)

Mari kita selesaikan persamaan ini dengan mengisolasi \(x\):

\[ 2x = 12 \]

\[ x = 6 \]

Jadi, nilai \(x\) untuk persamaan linier adalah 6.
