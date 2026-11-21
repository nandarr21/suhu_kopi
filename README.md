# TA-06 Pemodelan dan Simulasi — Simulasi Penurunan Suhu Kopi Panas

Model sistem dinamik secangkir kopi panas yang mendingin di udara ruang, dilengkapi *mug warmer*
sebagai sinyal kontrol.

Model (neraca energi, ODE orde-1):

    m·c·dT/dt = u(t) − h·A·(T − T∞)

| Parameter | Nilai |
|---|---|
| m (massa kopi) | 0,25 kg |
| c (kalor jenis) | 4180 J/(kg·K) |
| h (koef. perpindahan panas) | 12 W/(m²·K) |
| A (luas permukaan) | 0,03 m² |
| T∞ (suhu ruang) | 25 °C |
| T₀ (suhu awal) | 90 °C |

Skenario: pendinginan tanpa pemanas, steady state, sinyal step, impulse, ramp, sinusoida,
dan gangguan suhu ruang. Diselesaikan dengan metode Euler (Δt = 1 s) dan divalidasi dengan solusi analitik.

## Cara menjalankan

    pip install numpy matplotlib jupyter
    jupyter notebook TA06_Simulasi_Penurunan_Suhu_Kopi.ipynb

Grafik hasil simulasi otomatis tersimpan di folder `gambar/`.
