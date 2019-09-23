# Deploy Model Credit on My PythonAnywhere
url : http://firli.pythonanywhere.com/api <br>
kodingan pada server pythonanywhere: https://www.pythonanywhere.com/user/firliilhami/shares/bdc2720b1a8248bcb54d22062e3d06c5/
## 1. Penjelasan Model
Model ini adalah model untuk menentukan apakah seorang customer akan telat membayar tagihannya atau membayar tagihan tepat waktu. Model ini menggunakan metode regresi logistik yang merupakan binary model dimana output model kita hanya ada  2 yaitu :
* Label=0, berarti Customer ke n  tidak akan terlambat bayar
* Label=1, berarti Customer ke n  terlambat bayar

Model ini menggunakan 3 feature untuk memprediksi apakah orang tersebut akan telat membayar pada bulan depan, yaitu feature :
* BILL_AMT1 : Merupakan Tagihan pembayaran bulan ke 1
* BILL_AMT2 : Merupakan Tagihan pembayaran bulan ke 2
* BILL_AMT3 : Merupakan Tagihan pembayaran bulan ke 3

## 2. Run pada server PythonAnywhere
Model ini akan melakukan run 'flaskk_app.py' pada server pythonanywhere .
Pada server pythonanywhere diupload rf_model.pkl. yang merupakan model regresi logistik yang sudah dibuat dan sudah ditrain dengan data yang kita punya.

## 3. Test Model
Untuk mengetest model yang sudah kita deploy kita menggunakan POSTMAN

### Cara menggunakan POSTMAN :
1. HARUS menggunakan web browser google chrome karena akan menggunakan ekstension pada google chrome ( apabila sudah terdapat postman pada google chrome langsung ke poin '4'.
2. Pada mesin pencari google search 'Postman Chrome'
3. Pilih POSTMAN - Google Chrome  ( paling atas pada hasil pencarian )
3. Pilih add feature untuk menginstall chrome dan tunggu sampai instalasi selesai.
4. Buka ekstension POSTMAN
5. Tampilan postman akan seperti berikut
 ![](https://raw.githubusercontent.com/firliilhami/API/master/gambar%20postman.png)
7. Pada lingkaran yang berwarna oranye ubah menjadi POST
8. Pada kotak berwarna biru isi dengan url server saya yaitu http://firli.pythonanywhere.com/api
9. Pilih Body yaitu pada kotak berwarna coklat kemudian pilih raw.
10. Lalu inputan value yang diingiinkan dituliskan pada kotak bewarna kuning . Bagaimana cara menuliskan inputannya diberitahu pada bagian selanjutnya.
11. Terakhir klik Send

#### Bagaimana cara menuliskan inputnya
Jika hanya menginputkan 1 data customer :
* Contoh : [{ "BILL_AMT1":1000, "BILL_AMT2":1500, "BILL_AMT3":100000 }]

Jika menginput lebih dari 1 data customer contohnya dapat dilihat di data.txt dan bisa langsung di copy paste



