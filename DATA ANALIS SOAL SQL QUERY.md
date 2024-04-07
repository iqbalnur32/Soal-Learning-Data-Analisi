## ** SUMBER: https://github.com/LintangWisesa/Ujian_AnalyticsVisualization_JCDS08/blob/master/README.md**

Soal 1  ( Distrubition Die Cast )

# Soal Ujian Data Science - Data Analytics & Visualization

![Lintang_Purwadhika](https://static.wixstatic.com/media/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png/v1/fill/w_246,h_39,al_c,usm_0.66_1.00_0.01/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png)

## **Soal 1 - Distributor Die Cast 🚗**

![hotwheels](https://drimjuguetes.vteximg.com.br/arquivos/banner-landing-hotwheels.jpg)

Anda adalah distributor ternama di bidang jual-beli _die cast_ (miniatur moda transportasi) yang menjual beragam produk dari vendor-vendor berkualitas,
dengan 7 kantor cabang tersebar di beberapa negara dunia. Disediakan database
yang menyimpan berbagai data terkait usaha Anda, mulai dari daftar customer, karyawan, produk hingga transaksi yang dilakukan. 

Unduh database __.sql__ di repo ini ([_**/database/retrowheels.sql**_](/database)) dan import ke local MySQL server Anda. Tata cara import database juga tercantum di folder: ([_**/database**_](/database)). Kemudian selesaikan soal-soal berikut. Anda __dilarang keras__ mengubah struktur & format tabel serta database yang telah disediakan.

1. Rumuskan _single query_ untuk menampilkan jumlah __total customer__ yang Anda layani, beserta jumlah __total kota & negara asal__ customer-customer Anda. Contoh output yang diharapkan:

    ```bash
    +-----------+--------+-----------+
    | Customers | Cities | Countries |
    +-----------+--------+-----------+
    |       122 |     95 |        27 |
    +-----------+--------+-----------+
    ```

    Anda memiliki __122 customer__ dari __95 kota__ yang tersebar di __27 negara__!

2. Rumuskan _single query_ untuk menampilkan _resources_ yang Anda miliki, mulai dari jumlah __karyawan__, jumlah __kantor & lokasi negaranya__, jumlah __barang yang dijual__, total __stok barang__ & jumlah __vendor__ yang menjadi partner Anda. Contoh output yang diharapkan:

    ```bash
    +-----------+---------+---------+----------+---------------+---------+
    | Employees | Offices | Country | Products | StockProducts | Vendors |
    +-----------+---------+---------+----------+---------------+---------+
    |        23 |       7 |       5 |      110 |        555131 |      13 |
    +-----------+---------+---------+----------+---------------+---------+
    ```

    Anda memiliki __23 karyawan__ di __7 kantor__ yang berada di __5 negara__, dengan __110 model die cast__ (total stok mencapai __555131 item__) yang didistribusikan dari __13 vendor partner__.

3. Dari soal sebelumnya tercatat Anda memiliki __110 model die cast__ dengan total stok __555131 item__. Jika dikategorikan, produk yang Anda jual terbagi menjadi __7 product line__ _die cast_, yakni model mobil klasik, mobil _vintage_, sepeda motor, pesawat terbang, kapal laut, kereta api serta truk & bus. Rumuskan _single query_ yang dapat menampilkan __harga produk terendah & tertinggi__ untuk masing-masing kategori. Contoh output yang diharapkan:

    ```bash
    +------------------+----------+----------+
    | productLine      | minPrice | maxPrice |
    +------------------+----------+----------+
    | Classic Cars     |    15.91 |   103.42 |
    | Motorcycles      |    24.14 |    91.02 |
    | Planes           |    29.34 |    77.27 |
    | Ships            |    33.30 |    82.34 |
    | Trains           |    26.72 |    67.56 |
    | Trucks and Buses |    24.92 |    84.76 |
    | Vintage Cars     |    20.61 |    86.70 |
    +------------------+----------+----------+
    ```

4. Rumuskan _single query_ yang dapat menampilkan daftar 10 customer paling _royal_ (paling banyak mendatangkan uang bagi kita), yang total nominal transaksinya paling tinggi. Data yang ditampilkan adalah nama customer, kota & negara asal, beserta total uang yang dihabiskan di produk kita. Contoh output yang diharapkan:

    ```bash
    +------------------------------+---------------+-------------+-----------+
    | customerName                 | city          | country     | total     |
    +------------------------------+---------------+-------------+-----------+
    | Euro+ Shopping Channel       | Madrid        | Spain       | 715738.98 |
    | Mini Gifts Distributors Ltd. | San Rafael    | USA         | 584188.24 |
    | Australian Collectors, Co.   | Melbourne     | Australia   | 180585.07 |
    | Muscle Machine Inc           | NYC           | USA         | 177913.95 |
    | Dragon Souveniers, Ltd.      | Singapore     | Singapore   | 156251.03 |
    | Down Under Souveniers, Inc   | Auckland      | New Zealand | 154622.08 |
    | AV Stores, Co.               | Manchester    | UK          | 148410.09 |
    | Anna's Decorations, Ltd      | North Sydney  | Australia   | 137034.22 |
    | Corporate Gift Ideas Co.     | San Francisco | USA         | 132340.78 |
    | Saveley & Henriot, Co.       | Lyon          | France      | 130305.35 |
    +------------------------------+---------------+-------------+-----------+
    ```

5. Pada __2003-06-05__, terdapat pembayaran masuk sebesar __US$ 14571.44__. Tampilkan data seputar transaksi tersebut, mencakup __nama customer__ yang melakukan pembayaran, __nama produk__ yang dibeli, __jumlah tiap produk__ yang dibeli dan __harga satuannya__. Pastikan
total harga yang dibeli sesuai dengan data pembayaran masuk. Output yang diharapkan:

    ```bash
    +-------------------+--------------------------------+-----------------+-----------+
    | customername      | productname                    | quantityOrdered | priceEach |
    +-------------------+--------------------------------+-----------------+-----------+
    | Atelier graphique | 1965 Aston Martin DB5          |              26 |    120.71 |
    | Atelier graphique | 1999 Indy 500 Monte Carlo SS   |              46 |    114.84 |
    | Atelier graphique | 1948 Porsche Type 356 Roadster |              34 |    117.26 |
    | Atelier graphique | 1966 Shelby Cobra 427 S/C      |              50 |     43.27 |
    +-------------------+--------------------------------+-----------------+-----------+
    ```

    Jika Anda cek jumlah total dari ```quantityOrdered``` dikali ```priceEach``` dari tabel di atas, hasilnya __14571.44__. Dan transaksi pembayaran tersebut terjadi tepat pada tanggal __2003-06-05__.

## **Jawaban**

  1. select count(customerName), count(DISTINCT city), count(DISTINCT country) from customers;
  2. select Employes, Offices, Country, Product, Stock, Vendor from (select count(e.employeeNumber) as Employes, count(DISTINCT o.officeCode) as Offices, count(DISTINCT o.country) as Country from offices o INNER JOIN employees e ON o.officeCode = e.officeCode ) as t1 CROSS JOIN ( select count(p.productCode) as Product, sum(p.quantityInStock) as Stock, count(DISTINCT p.productVendor) as Vendor from products p ) as t2;
      [
          select 
            Employes,
            Offices,
            Country,
            Product,
            Stock,
            Vendors
          from 
            (select 
              count(e.employeeNumber) as Employes, 
              count(DISTINCT o.officeCode) as Offices, 
              count(DISTINCT o.country) as Country
            from 
              offices o
            INNER JOIN
              employees e ON o.officeCode = e.officeCode
            ) as t1
          CROSS JOIN 
            (
              select 
                count(p.productCode) as Product, 
                sum(p.quantityInStock) as Stock, 
                count(DISTINCT p.productVendor) as Vendors
              from 
                products p
            ) as t2
      ]
  3. select products.productLine, MIN(buyPrice) as minPrice, MAX(buyPrice) as minPrice from products JOIN productlines ON products.productLine = productlines.productLine GROUP BY products.productLine;
  4. select customers.customerName, customers.city, customers.country, sum(payments.amount) as total from customers JOIN payments ON customers.customerNumber = payments.customerNumber group by customers.customerNumber order by total desc limit 10;
  5. select customers.customerName, products.productName, orderdetails.quantityOrdered, orderdetails.priceEach from customers JOIN orders ON customers.customerNumber = orders.customerNumber JOIN orderdetails ON orders.orderNumber = orderdetails.orderNumber JOIN products ON orderdetails.productCode = products.productCode WHERE orders.orderDate = '2003-05-20';
