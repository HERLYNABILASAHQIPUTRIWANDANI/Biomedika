---
title: Biomedika

---
# BIOMEDIKA
1. Matriks Awal

$$
\
\begin{bmatrix}
237 & 236 & 232 & 225 \\
231 & 230 & 228 & 225 \\
224 & 224 & 223 & 223 \\
221 & 221 & 219 & 217
\end{bmatrix}
$$

2. Kuantisasi ke 8 Level

$$
g = \left\lfloor \frac{f(x,y)}{32} \right\rfloor
$$

$$
\
\begin{bmatrix}
7 & 7 & 7 & 7 \\
7 & 7 & 7 & 7 \\
7 & 7 & 6 & 6 \\
6 & 6 & 6 & 6
\end{bmatrix}
\
$$

3. Matriks GLCM $$(0^\circ)$$

$$
\
P(i,j) =
\begin{bmatrix}
0.333 & 0 \\
0.083 & 0.583
\end{bmatrix}
\
$$

4. Perhitungan Fitur

a. Contrast

$$
\text{Contrast} = \sum_{i,j} (i - j)^2 \, P(i,j)
$$

$$
= (6-6)^2(0.333) + (7-6)^2(0.083) + (7-7)^2(0.583)
$$

$$
= 0 + 0.083 + 0 = 0.083
$$

b. Homogeneity

$$
\text{Homogeneity} = \sum_{i,j} \frac{P(i,j)}{1 + |i - j|}
$$

$$
= \frac{0.333}{1 + 0} + \frac{0.083}{1 + 1} + \frac{0.583}{1 + 0}
$$

$$
= 0.333 + 0.0415 + 0.583 = 0.9575
$$

c. Energy

$$
\text{Energy} = \sum_{i,j} P(i,j)^2
$$

$$
= (0.333)^2 + (0.083)^2 + (0.583)^2
$$

$$
= 0.110 + 0.0069 + 0.340 = 0.4569
$$

d. Correlation

Mean:

$$
\mu = \sum_{i,j} i \, P(i,j)
$$

$$
= 6(0.333) + 7(0.083 + 0.583)
$$

$$
= 1.998 + 4.662 = 6.66
$$

Variance:

$$
\sigma^2 = \sum_{i,j} (i - \mu)^2 P(i,j)
$$

$$
= (6-6.66)^2(0.333) + (7-6.66)^2(0.666)
$$

$$
= 0.145 + 0.077 = 0.222
$$

$$
\sigma = \sqrt{0.222} = 0.471
$$

Correlation:

$$
\text{Correlation} =
\frac{\sum_{i,j} (i - \mu)(j - \mu) P(i,j)}{\sigma^2}
$$

$$
= \frac{0.145 - 0.0186 + 0.067}{0.222}
= 0.87
$$

5. Hasil Akhir

$$
\begin{aligned}
\text{Contrast} &= 0.083 \\
\text{Homogeneity} &= 0.957 \\
\text{Energy} &= 0.457 \\
\text{Correlation} &= 0.87
\end{aligned}
$$

Kesimpulan

Berdasarkan hasil perhitungan GLCM dari matriks citra MRI:

- Nilai contrast rendah (0.083) menunjukkan perbedaan intensitas antar piksel kecil
- Nilai homogeneity tinggi (0.957) menunjukkan tekstur citra sangat seragam
- Nilai energy cukup tinggi (0.457) menunjukkan pola piksel teratur
- Nilai correlation tinggi (0.87) menunjukkan hubungan antar piksel kuat

Hal ini menandakan bahwa area yang dianalisis memiliki tekstur halus, seragam, dan intensitas tinggi, yang merupakan karakteristik dari area tumor pada citra MRI.