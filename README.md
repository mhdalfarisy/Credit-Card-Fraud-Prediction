# Credit-Card-Fraud-Prediction

Sumber Data : https://www.kaggle.com/datasets/dhanushnarayananr/credit-card-fraud


![df](https://github.com/mhdalfarisy/Credit-Card-Fraud-Prediction/blob/main/68747470733a2f2f65787465726e616c2d636f6e74656e742e6475636b6475636b676f2e636f6d2f69752f3f753d687474707325334125324625324661692d6a6f75726e65792e636f6d25324677702d636f6e74656e7425324675706c6f61647325324632303139253246.jfif)

- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Analytical Approach](#analytical-approach)
- [Definisi Kolom](#definisi-kolom)
- [Kesimpulan](#kesimpulan)
- [Saran](#saran)
- [Others Project](#others-project)
  

### **Problem Statement**
  - Menurut beberapa sumber terkenal, diperkirakan 10.000 transaksi terjadi melalui kartu kredit setiap detik di seluruh dunia. Karena frekuensi transaksi yang begitu tinggi, kartu kredit menjadi sasaran utama penipuan.

Setiap tahun, miliaran dolar hilang secara langsung karena penipuan kartu kredit. Kasus penipuan terjadi dalam kondisi yang berbeda, misalnya, transaksi di tempat penjualan (POS) atau transaksi yang dilakukan secara online atau melalui telepon, misalnya kasus kartu tidak ada (CNP) atau transaksi dengan kartu yang hilang dan dicuri. Dengan cara ini, penipuan kartu kredit pada tahun 2015 saja berjumlah 21,84 miliar dolar, dengan penerbit menanggung biaya 15,72 miliar dolar.

Banyak survei menunjukkan bahwa peningkatan ketergantungan pada kartu kredit untuk melakukan transaksi keuangan disertai dengan peningkatan tingkat penipuan.

Peningkatan penipuan kartu kredit baru-baru ini secara langsung memukul sektor keuangan dengan keras. Kerugian akibat penipuan kartu kredit terutama berdampak pada pedagang karena mereka menanggung semua biaya, termasuk biaya dari penerbit kartu mereka, biaya administrasi dan biaya lainnya. Semua kerugian ditanggung oleh pedagang, yang menyebabkan kenaikan harga barang dan penurunan diskon. Oleh karena itu, mengurangi kerugian ini sangat penting. Diperlukan sistem deteksi fraud yang efektif untuk meminimalisir jumlah kasus fraud.. 

### **Objectives**
  - Analisa ini akan berfokus mendeteksi hal apa yang paling berpengaruh dalam pencurian kartu kredit ini sehingga perusahaan jasa keuangan (Perbankan) dapat melakukan evaluasi terhadap tindak kriminal ini.
  
### **Metric**
- 0 = Non-Fraud (Negative)
- 1 = Fraud (Positive)

- Error tipe 1: False Positive
- False Positive akan memberikan prediksi jumlah tidak terjadinya kasus kriminal pencurian kartu kredit namun pada realitanya terjadi kecurangan pencurian kartu kredit, hal ini jika dibiarkan maka akan menyebabkan semakin tinggi tingkat pencurian kartu kredit dan beresiko menyebabkan konsumen kehilangan kepercayaan pada perbankan.

- Error Tipe 2: False Negative
- False Negatif akan memberikan prediksi jumlah tindakan kasus kriminal pencurian kartu kredit namun pada realitanya tidak terjadi kecurangan pencurian kartu kredit, hal ini akan menyebabkan perusahaan sering mendapatkan komplain dari customer terkait laporan - laporan transaksi customer.

Berdasarkan konsekuensinya, maka sebisa mungkin model yang akan dibuat dapat membantu pihak perbankan dan customer dalam mengecilkan pencurian kartu kredit tanpa merugikan perbankan dari segi nama baik perbankan dan tanpa mengganggu transaksi konsumen sehingga penggunaan machine learning ini dapat membantu kedua pihak. Maka dari itu , nilai recall dan precision berdasarkan kelas positifnya perlu untuk di seimbangkan sehingga metric utama yang akan digunakan adalah `f-1 score`.

### **Analytical Approach**
  - Dalam analisa ini akan dilakukan 3 tahapan :
  - 1. Tahapan pertama akan melakukan Exploratory Data Analyst untuk mendapatkan insight secara deskriptive
  - 2. Tahapan kedua akan melakukan visualisasi dari hasil data yang sudah di analisa
  - 3. Tahapan ketiga akan melakukan modeling machine learning sehingga diperoleh faktor apa yang memiliki pengaruh penyebab terjadinya tindakan kriminal pencurian kartu kredit sehingga perusahaan dapat menargetkan berapa total nasabah yang akan dicegah dari tindakan kecurangan pencurian kartu kredit ini.

### **Definisi Kolom**
#

| **Nama Kolom** | **Keterangan Kolom** |
| --- | --- |
|**Credit Card Fraud**||
|Distance From Home| The distance from home where the transaction happened|
|Distance From Last Transaction| The distance from last transaction happened|
|Ratio To Median Purchase Price| Ratio of purchased price transaction to median purchase price|
|Repeat Retailer|  Is the transaction happened from same retailer|
|Used Chip |  Is the transaction through chip (credit card)|
|Used Pin Number| Is the transaction happened by using PIN number|
|Online Order | Is the transaction an online order|
|Fraud | Is the transaction fraudulent|


### **Kesimpulan**

1.	Transaksi kecurangan terjadi sebanyak 8,7%, yang mana lokasi terbanyak terjadi berada kurang dari  27mil dari jarak rumah, hal ini terjadi pada transaksi pada toko yang pernah kostumer kunjungi untuk berbelanja secara online dan transaksi kecurangan pada kartu kredit ini terjadi pada kartu kredit yang tidak memiliki pin keamanan tambahan dan kartu kredit yang tidak menggunakan chip dan untuk kecurangan ini paling banyak pada harga kurang dari 20USD atau masuk dalam kategori transaksi dengan harga yang sedang.
2.	Dari kasus ini hal yang paling memiliki pengaruh ada pada harga pembelian dengan total persentase pengaruh nya 5%.
3.	Model Machine Learning ini menggunakan algoritma XGBoost dan hasil dari prediksi machine learning ini mampu menebak transaksi yang teridentifikasi tidak melakukan kecurangan sebanyak 99%, dan transaksi yang dianggap memiliki resiko kecurangan sebanyak 89%, transaksi yang sama sekali tidak termasuk dalam kecurangan sebanyak 99% dan rata-rata keberhasilan menebak ada pada angka 94% keakuratannya serta model machine learning ini secara keseluruhan memiliki persentase keakuratan secara keseluruhan sebanyak 91%.

### **Saran**

- Pihak perbankan dapat meningkatkan standar keamanan pada penggunaan kartu kredit terutama pada kartu kredit yang belum menggunakan kartu yang memiliki chip dan yang belum memiliki tambahan pin saat penggunaan kartu kredit.
- Jika model machine learning ini di implementasikan maka tingkat keamanan untuk mendeteksi kecurangan penggunaan kartu kredit akan menurun namun pihak perbankan tetap harus memberikan notifikasi / konfirmasi tambahan kepada konsumen setiap transaksi yang dilakukan. Hal ini dilakukan untuk mengefisienkan penggunaan machine learning ketika melakukan pendeteksian kecurangan kartu kredit, Karena jika hal ini tidak di implementasikan jika transaksi yang dilakukan customer terutama untuk harga pembeliannya diatas rata-rata transaksi yang biasanya maka machine akan mendeteksi telah terjadi kecurangan dan customer akan mendapatkan notifikasi telah terjadi kecurangan. Sehingga untuk meng efisienkan dan meng efektifkan penggunaan nya perlu dilakukan kerja sama antara perbankan dengan customer seperti menambah fitur konfirmasi tambahan untuk setiap transaksi yang menyatakan bahwa transaksi tersebut dilakukan oleh customer dan konfirmasi ini dilakukan melalui aplikasi perbankan yang ada di mobil customer serta jika customer tidak melakukan transaksi maka perbankan tidak dapat meneruskan transaksi tersebut hal ini untuk menghindari dan mengecilkan transaksi yang curang pada kartu kredit customer.

<br>

<br>

# **OTHERS PROJECT**

**My Project :** [Data Analyst](#data-analyst) | [Machine Learning](#machine-learning) | [Data Visualization](#data-visualization)

**Tech stacks currently using** <br>

<code><a href="https://code.visualstudio.com/" target="_blank"><img height="50" src="https://www.vectorlogo.zone/logos/visualstudio_code/visualstudio_code-ar21.svg"></a></code>
<code><a href="https://jupyter.org/" target="_blank"><img height="50" src="https://www.vectorlogo.zone/logos/jupyter/jupyter-ar21.svg"></a></code>
<code><a href="https://www.python.org/" target="_blank"><img height="50" src="https://www.vectorlogo.zone/logos/python/python-ar21.svg"></a></code>
<code><a href="https://www.mysql.com/" target="_blank"><img height="50" src="https://www.vectorlogo.zone/logos/mysql/mysql-ar21.svg"></a></code>
<code><a href="https://www.microsoft.com/en-us/sql-server/sql-server-downloads" target="_blank"><img height="50" src="https://cdn.worldvectorlogo.com/logos/microsoft-sql-server-1.svg"></a></code>
<code><a href="https://www.postgresql.org/" target="_blank"><img height="50" src="https://www.vectorlogo.zone/logos/postgresql/postgresql-ar21.svg"></a></code>
<code><a href="https://powerbi.microsoft.com/en-us/" target="_blank"><img height="50" src="https://www.vectorlogo.zone/logos/microsoft_powerbi/microsoft_powerbi-ar21.svg"></a></code>
<code><a href="https://public.tableau.com/app/profile/muhammad.al.farisy6147" target="_blank"><img height="30" src="https://cdn.worldvectorlogo.com/logos/tableau-logo.svg"></a></code>
<br>
<br>
<table>
<tbody>
 <tr>

<h1 align="left">Data Analyst</h1>
  
<td align="left" width="50%">
<span><b><Left>E-Commers Pakistan</center></b></span> 
<code><a href="https://github.com/mhdalfarisy/EDA---Pakistan-s-Larges-Ecommers" target="_blank">
<img height=250px src="https://github.com/mhdalfarisy/EDA---Pakistan-s-Larges-Ecommers/blob/main/Images/62253a402fccf.jpg"> 
</td>
<!-- <tr> -->
<td align="left" width="50%">
<span><b><Left>Employee Attrition</center></b></span> 
<code><a href="https://github.com/mhdalfarisy/Employee-Analysis-Attrition-Report" target="_blank">
<img height=250px src="https://github.com/mhdalfarisy/Employee-Analysis-Attrition-Report/blob/main/Aset/Reasons-Attrition1_large%20(1).jpg"> 
</td>
</tbody>
</table>
 <tr>
<br>
<table>
<tbody>
 <tr>
 
<h1 align="left">Machine Learning - Supervised</h1>

<td align="left" width="20%">
<span><b><left>California House Price</center></b></span> 
<code><a href="https://github.com/mhdalfarisy/California-House-Price-Prediction-Using-Machine-Learning" target="_blank">
<img height=150px src="https://github.com/mhdalfarisy/California-House-Price-Prediction-Using-Machine-Learning/blob/main/gambar/CA-Sales-Home-Volume.png"> 
</td>

<td align="left" width="20%">
<span><b><left>Credit Card Fraud</center></b></span> 
<code><a href="https://github.com/mhdalfarisy/Credit-Card-Fraud-Prediction" target="_blank">
<img height=150px src="https://github.com/mhdalfarisy/Credit-Card-Fraud-Prediction/blob/main/68747470733a2f2f65787465726e616c2d636f6e74656e742e6475636b6475636b676f2e636f6d2f69752f3f753d687474707325334125324625324661692d6a6f75726e65792e636f6d25324677702d636f6e74656e7425324675706c6f61647325324632303139253246.jfif"> 
</td>

<!-- <tr> -->
<td align="left" width="20%">
<span><b><left>Telco Customer Churn</center></b></span> 
<code><a href="https://github.com/mhdalfarisy/Employee-Promotion" target="_blank">
<img height=150px src="https://github.com/mhdalfarisy/mhdalfarisy/blob/main/7-Strategies-To-Reduce-Customer-Churn-Rate.png"> 
</td>

<!-- <tr> -->
<td align="left" width="20%">
<span><b><left>Employee Promotion</center></b></span> 
<code><a href="https://github.com/mhdalfarisy/Telco-Customer-Churn-Predict" target="_blank">
<img height=150px src="https://github.com/mhdalfarisy/mhdalfarisy/blob/main/advance-career.jpg"> 
</td>

</tbody>
</table>
 <tr>
  
<h1 align="left">Machine Learning - Unsupervised</h1>  

<table>
<tbody>
 <tr>  
  
<!-- <tr> -->
<td align="center" width="30%">
<span><b><left>Segmentation Customer Mall</center></b></span> 
<code><a href="https://github.com/mhdalfarisy/Segmentation-Customer-Mall" target="_blank">
<img height=250px src="https://github.com/mhdalfarisy/Segmentation-Customer-Mall/blob/main/2.-Customer-Segmentation.jpg"> 
</td>
 
<!-- <tr> -->
<td align="center" width="30%">
<span><b><left>Segmentation Customer Supermarket</center></b></span>
<code><a href="https://github.com/mhdalfarisy/Customer-Supermarket" target="_blank">
<img height=250px src="https://github.com/mhdalfarisy/mhdalfarisy/blob/main/istockphoto-1254636143-612x612.jpg"> 
</td> 

<!-- <tr> -->
<td align="center" width="30%">
<span><b><left>Segmentation German Credit Risk</center></b></span>
<code><a href="https://github.com/mhdalfarisy/German-Credit-Risk" target="_blank">
<img height=250px src="https://media.istockphoto.com/vectors/banking-credit-card-vector-id1353716726?b=1&k=20&m=1353716726&s=612x612&w=0&h=qkwNRlcHCDUxeSgVYau8FczoM6x0sl693nvjAAcRmio="> 
</td> 
 
</tbody>
</table>
 <tr>
  
<br>

<table>
<tbody>
 <tr>

<h1 align="left">Data Visualization</h1>
  
<td align="left" width="20%">
<span><b><Left>E-Commers Pakistan</center></b></span> 
<code><a href="https://public.tableau.com/app/profile/muhammad.al.farisy6147/viz/ProjectE-CommersPakistanDashboard/Dashboard1" target="_blank">
<img height=200px src="https://github.com/mhdalfarisy/mhdalfarisy/blob/main/Pakistan%20Visualisasi.png"> 
</td>
 
<!-- <tr> -->
<td align="left" width="30%">
<span><b><left>Employee Attrition Report</center></b></span> 
<code><a href="https://public.tableau.com/app/profile/muhammad.al.farisy6147/viz/ProjectHumanResourceAttritionAnalysisDashboard/Dashboard1" target="_blank">
<img height=200px src="https://github.com/mhdalfarisy/mhdalfarisy/blob/main/HRD%20VIsualisasi.png"> 
</td>
 
<!-- <tr> -->
<td align="left" width="25%">
<span><b><left>Telco Customer Churn</center></b></span> 
<code><a href="https://public.tableau.com/app/profile/muhammad.al.farisy6147/viz/CustomerChunVisualization/Dashboard2?publish=yes" target="_blank">
<img height=200px src="https://github.com/mhdalfarisy/mhdalfarisy/blob/main/Telco%20Customer%20Churn.png"> 
</td>
 
</tbody>
</table>
 <tr>



<br>
<!-- <h1 align="center">Others Data Visualization Report</h1> -->
<td align="left" width="30%">
<span><b><left>Others Data Visualization Report (Click Picture) :   </left></b></span> 
<code><a href="https://public.tableau.com/app/profile/muhammad.al.farisy6147" target="_blank"><img height="100" src="https://github.com/mhdalfarisy/mhdalfarisy/blob/main/tol_devices_optimized.png"></a></code>
<br>
<br>
<br>
 
**💬 Ask me about anything, I'll be happy to help!** <br>
**💬 My inbox is always open, Contact me**
<br>
<br> 
  </a>
  <a href="mailto:m.alfarisy797@gmail.com">
    <img align="left" alt="Muhammad Al-farisy | Gmail" width="26px" src="https://cdn.worldvectorlogo.com/logos/official-gmail-icon-2020-.svg" />
  </a>
  <a href="https://www.linkedin.com/in/m-alfarisy97/">
    <img align="left" alt="Muhammad Al-farisy | LinkedIN" width="26px" src="https://cdn.worldvectorlogo.com/logos/linkedin-icon-2.svg" />    
  </a>
<br>
<br>


| <a href="https://github.com/mhdalfarisy"><img align="center" src="https://github-readme-stats.vercel.app/api?username=mhdalfarisy&show_icons=true&include_all_commits=true&theme=buefy&hide_border=true" alt="Anurag's github stats" /></a> | <a href="https://github.com/mhdalfarisy/github-readme-stats"><img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=mhdalfarisy&layout=compact&theme=buefy&hide_border=true" /></a> |
| ------------- | ------------- |
 
<table>
<tbody>
 <tr>
 
<h1 align="left">THANKS YOU !!! </h1>

<td align="center" width="30%">
<img height=300px src="https://media.giphy.com/media/dyzew7Py7bnW9DiJJj/giphy.gif"> 
</td>  
  
<!-- <td align="center" width="30%">
<img height=300px src="https://media.giphy.com/media/7c8QeB0VMddFOuu4iR/giphy.gif"> 
</td>
  
<td align="right" width="30%">
<img height=300px src="https://media.giphy.com/media/gutZ5Pm6Xl62eIf5RZ/giphy.gif"> 
</td>    -->

⭐️ From [Muhammad Al-farisy](https://github.com/mhdalfarisy)

