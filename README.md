# bitcoin-price

# Bitcoin Data
# import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import seaborn as sns
# Latihan 1 : Bitcoin Price
prices = [14292.2, 12858.9, 11467.5, 9241.1, 8559.6, 11073.5,
9704.3, 11402.3,
8762.0, 7874.9, 8547.4, 6938.2, 6905.7, 8004.4, 8923.1,
9352.4,
9853.5, 8459.5, 8245.1, 7361.3, 7646.6, 7515.8, 6505.8,
6167.3,
6398.9, 6765.5, 6254.8, 7408.7, 8234.1, 7014.3, 6231.6,
6379.1,
6734.8, 7189.6, 6184.3, 6519.0, 6729.6, 6603.9, 6596.3,
6321.7,
6572.2, 6494.2, 6386.2, 6427.1, 5621.8, 3920.4, 4196.2,
3430.4,
3228.7, 3964.4, 3706.8, 3785.4,] 
          
          
prices2019 = [3597.2, 3677.8, 3570.9,
3502.5,
3661.4, 3616.8, 4120.4, 3823.1, 3944.3, 4006.4, 4002.5,
4111.8,
5046.2, 5051.8, 5290.2, 5265.9, 5830.9, 7190.3, 7262.6,
8027.4,
8545.7, 7901.4, 8812.5, 10721.7, 11906.5, 11268.0,
11364.9, 10826.7,
9492.1, 10815.7, 11314.5, 10218.1, 10131.0, 9594.4,
10461.1, 10337.3,
9993.0, 8208.5, 8127.3, 8304.4, 7957.3, 9230.6, 9300.6,
8804.5,
8497.3, 7324.1, 7546.6, 7510.9, 7080.8, 7156.2, 7321.5,
7376.8]
plt.plot(prices)
plt.plot(prices2019, linestyle='--')
plt.title('Bitcoin prices 2018 & 2019')
plt.ylabel('Prices')
plt.xlabel('Weeks')
plt.legend(['2018', '2019'])
plt.show()
# Penjelasan :
1) Chart apa yang anda pilih untuk problem diatas dan mengapa anda memilih chart tersebut?

•	Line Chart karena diagram garis lebih baik untuk menunjukkan bagaimana kemajuan data selama berberapa periode.

2) Tahun berapa pemegang bitcoin memiliki keuntungan yang lebih banyak?

•	Tahun 2019, karena harganya cenderung naik dibandingkan dengan harga disaat awal minggu. Meskipun setelah di minggu 25 tahun 2019 harganya turun, tetapi tetap lebih tinggi jika dibandingkan dengan harga bitcoin di awal 2x minggu tahun 2019. Jika investor membeli di minggu pertama tahun 2019, meskipun di minggu ke 52 harganya turun tetap mengalami keuntungan.
# Latihan 2 : Permen
candy_names = ['Kit Kat', 'Snickers', 'Milky Way', 'Toblerone',
'Twix']
candy_counts = [52, 39, 78, 13, 78]
colors = ('#008B8B', '#FF8C00', '#7FFF00', '#00FFFF', '#FF1493')
explode = (0, 0.1, 0, 0, 0)
plt.title('Jenis Permen')
plt.pie(
    candy_counts,
    labels=candy_names,
    autopct='%1.1f%%',
    colors=colors,
    explode=explode,)
plt.show()
# Penjelasan :
3)	Chart apa yang anda pilih untuk problem diatas dan mengapa anda memilih chart tersebut?

•	Pie chart karena sangat cocok digunakan untuk menganalisis seberapa banyak dari setiap jenis kategori dalam dataset berbanding dengan keseluruhan.

4)	Berapa persen kemungkinan anda akan memilih snickers saat mengeluarkan permen dari tas secara acak?

•	n(permen) = 280

•	p(snickers) = 39/280 = 0.15

# Latihan 3 : Makanan
desert = ('Lava Cake', 'Mousse', 'Chocolate Cake', 'Ice Cream', 'Truffles', 'Brownie',
          'Chocolate Chip Cookie','Chocolate Pudding', 'Souffle', 'Chocolate Cheesecake',
         'Chocolate Chips', 'Fudge', 'Mochi')
sales = (14, 5, 12, 19, 6, 8, 12, 9, 10, 17, 2, 9, 13)
df = pd.DataFrame({
'Desert': desert,
'Sales': sales,
})
df.sort_values(by='Sales', inplace=True)
x_coords = np.arange(len(df))
colors = ['#0000FF' for _ in range(len(df))]
colors[0] = '#FF0000'
colors[1] = '#FF0000'
colors[2] = '#FF0000'
plt.figure(figsize=(20,10))
plt.bar(x_coords, df['Sales'], tick_label=df['Desert'],
color=colors)
plt.xticks(rotation=90)
plt.ylabel('Count of Sales')
plt.title('Fav Desert Sales')
plt.show()
# Penjelasan :
1)	Chart apa yang anda pilih untuk problem diatas dan mengapa anda memilih chart tersebut?

•	Bar Chart karena sangat cocok untuk memvisualisasaikan perbandingan data kategorikal

2)	Makanan penutup apa saja yang perlu anda sarankan untuk dikeluarkan dari menu?

•	Chocolate chips, Mousse, Truffles, karena jumlah penjualan sangat sedikit dibandingkan 10 menu lainnya.

# Latihan 4 : Penggunaan CPU
day = ['Monday','Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturdaay', 'Sunday']
cpu_usage = [
[2, 2, 4, 2, 4, 1, 1, 4, 4, 12, 22, 23,
45, 9, 33, 56, 23, 40, 21, 6, 6, 2, 2, 3], # Monday
[1, 2, 3, 2, 3, 2, 3, 2, 7, 22, 45, 44,
33, 9, 23, 19, 33, 56, 12, 2, 3, 1, 2, 2], # Tuesday
[2, 3, 1, 2, 4, 4, 2, 2, 1, 2, 5, 31,
54, 7, 6, 34, 68, 34, 49, 6, 6, 2, 2, 3], # Wednesday
[1, 2, 3, 2, 4, 1, 2, 4, 1, 17, 24, 18,
41, 3, 44, 42, 12, 36, 41, 2, 2, 4, 2, 4], # Thursday
[4, 1, 2, 2, 3, 2, 5, 1, 2, 12, 33, 27,
43, 8, 38, 53, 29, 45, 39, 3, 1, 1, 3, 4], # Friday
[2, 3, 1, 2, 2, 5, 2, 8, 4, 2, 3,
1, 5, 1, 2, 3, 2, 6, 1, 2, 2, 1, 4, 3], # Saturday
[1, 2, 3, 1, 1, 3, 4, 2, 3, 1, 2,
2, 5, 3, 2, 1, 4, 2, 45, 26, 33, 2, 2, 1], # Sunday
]
sns.heatmap(
cpu_usage,
yticklabels=day,
cmap='coolwarm',
)
# Penjelasan :
1)	Chart apa yang anda pilih untuk problem diatas dan mengapa anda memilih chart tersebut?

•	Heatmap karena dapat digunakan untuk memeriksa data secara visual guna menemukan kelompok dengan nilai serupa dan mendeteksi tren dalam data.

2)	Jam berapa pekerja biasa makan siang?

•	Jam 13.00 karena di area CPU tidak digunakan, ditunjukkan berdasarkan warna biru artinya cool/ suhu rendah.

3)	Apakah pekerja tersebut bekerja di akhir pekan?

•	Pada hari sabtu aktivitas CPU sangat rendah, jadi bisa dipastikan pada hari sabtu tidak ada pekerja yang masuk. Sedangkan pada hari minggu hanya dimalam hari yaitu 18.00 – 20.00

4)	Pada hari apa pekerja mulai bekerja pada computer mereka pada malam hari?

•	Mulai bekerja di waktu malam jam 18.00 : hari rabu, kamis, dan jumat.

# Latihan 5 : Jamur
x = [4.61, 5.08, 5.18, 7.82, 10.46, 7.66, 7.6, 9.32, 14.04, 9.95,
4.95, 7.23,
5.21, 8.64, 10.08, 8.32, 12.83, 7.51, 7.82, 6.29, 0.04, 6.62,
13.16, 6.34,
0.09, 10.04, 13.06, 9.54, 11.32, 7.12, -0.67, 10.5, 8.37, 7.24,
9.18,
10.12, 12.29, 8.53, 11.11, 9.65, 9.42, 8.61, -0.67, 5.94, 6.49,
7.57, 3.11,
8.7, 5.28, 8.28, 9.55, 8.33, 13.7, 6.65, 2.4, 3.54, 9.19, 7.51,
-0.68,
8.47, 14.82, 5.31, 14.01, 8.75, -0.57, 5.35, 10.51, 3.11, -
0.26, 5.74,
8.33, 6.5, 13.85, 9.78, 4.91, 4.19, 14.8, 10.04, 13.47, 3.28]

y = [-2.36, -3.41, 13.01, -2.91, -2.28, 12.83, 13.13, 11.94, 0.93, -
2.76, 13.31,
-3.57, -2.33, 12.43, -1.83, 12.32, -0.42, -3.08, -2.98, 12.46,
8.34, -3.19,
-0.47, 12.78, 2.12, -2.72, 10.64, 11.98, 12.21, 12.52, 5.53,
11.72, 12.91,
12.56, -2.49, 12.08, -1.09, -2.89, -1.78, -2.47, 12.77, 12.41,
5.33, -3.23,
13.45, -3.41, 12.46, 12.1, -2.56, 12.51, -2.37, 12.76, 9.69,
12.59, -1.12,
-2.8, 12.94, -3.55, 7.33, 12.59, 2.92, 12.7, 0.5, 12.57, 6.39,
12.84,
-1.95, 11.76, 6.82, 12.44, 13.28, -3.46, 0.7, -2.55, -2.37,
12.48, 7.26,
-2.45, 0.31, -2.51]
plt.title('Jamur')
plt.xlabel('Koordinat (X)')
plt.ylabel('Koordinat (Y)')
plt.scatter(x,y, color='y')
plt.show()
# Penjelasan :
1)	Chart apa yang anda pilih untuk problem diatas dan mengapa anda memilih chart tersebut?

•	Scatter Plot karena dapat memberikan informasi mengenai pola atau pencilan dua kelompok numerik.

2)	Koordinat pusat (x,y) pusat pertumbuhan jamur berada di?

•	Letak pusat pertumbuhan jamur adalah 7.64 , 5.13

