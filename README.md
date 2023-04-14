### **Nama**      : Rijal Ammar
### **Kelas**     : TI -3B
### **Tugas**      : Pertemuan 5
# 

# Screenshot dan Penjelasan

<table>
  <tr align="center">
    <td>
    Accumulator
    <td> <img src="https://user-images.githubusercontent.com/75898886/231911903-b7ad3f23-4864-4c50-9b8d-6386c68abc3c.png" width=70% height=70%><br>
        Kode tersebut membuat sebuah variabel accumulator yang dinamakan myaccum dengan nilai awal 0 menggunakan metode sc.accumulator yang disediakan oleh SparkContext sc. Kemudian membuat sebuah RDD  dinamakan myrdd dengan memparallelkan kisaran angka dari 1 hingga 99. Fungsi lambda yang dilewatkan ke operasi foreach menambahkan nilai dari setiap elemen ke dalam accumulator myaccum. Mencetak nilai dari accumulator menggunakan metode value. Output dari kode tersebut adalah jumlah dari semua elemen dalam RDD, yang bernilai 4950.
    </td>
    </td>
    </tr>
    <tr align="center">
    <td>    
    Broadcast
    <td><img src="https://user-images.githubusercontent.com/75898886/231912041-97f6033a-cbf8-4536-9771-5a49e0d03da7.png" width=70% height=70%><br>
  Kode tersebut membuat variabel broadcastVar dengan daftar bilangan bulat dari 1 hingga 99 menggunakan metode sc.broadcast.
  </td>
    </td>
    </tr>
    <tr align="center">
    <td>
    PairRDD
    <td><img src="https://user-images.githubusercontent.com/75898886/231912150-d5626885-c39b-4f4d-8945-9c03176120a3.png" width=70% height=70%><br>
      Kode tersebut membuat sebuah RDD bernama myRDD dengan tiga elemen menggunakan metode parallelize dari SparkContext sc. Selanjutnya, sebuah Pair RDD dengan nama myPairRDD dibuat dari myRDD dengan menggunakan metode map. Fungsi lambda yang dilewatkan ke metode map akan mengembalikan tuple yang terdiri dari elemen RDD dan panjangnya.
  </td>
    </td>
    </tr>
    <tr align="center">
    <td>
    WordCount
    <td>
      <img src="https://user-images.githubusercontent.com/75898886/231917391-853a4c09-73cc-41c3-a063-004a1e5a1173.png" width=70% height=70%><br>
       Membaca file README.md menggunakan metode textFile dari SparkContext sc. Teks dalam file tersebut dibagi menjadi kata-kata dengan. Setiap kata dalam RDD tersebut akan dibuat menjadi tuple dengan nilai awal 1 melalui fungsi map.Hasil penghitungan jumlah kemunculan kata-kata disimpan dalam variabel output menggunakan metode collect, dan kemudian dicetak ke layar menggunakan for loop untuk mengiterasi setiap kata dan jumlah kemunculan dalam variabel output.
  </td>
    </td>
        </tr>
    <tr align="center">
    <td>
    SystemCommandsReturnCode
         <td>
      <img src="https://user-images.githubusercontent.com/75898886/231917905-ada15735-b396-4749-bb27-01a76380550b.png"width=70% height=70%>
      <img src="https://user-images.githubusercontent.com/75898886/231917952-591c2a65-912b-45aa-9740-a2dbef107ddc.png" width=70% height=70%><br>
 Perintah ls /tmp dijalankan menggunakan  operator dan disimpan dalam variabel res. Hasil dari perintah tersebut akan dicetak ke layar dengan menggunakan println. Jika perintah berhasil dijalankan, maka nilai variabel res akan sama dengan 0 jika tidak non zero.
  </td>
    </td>    
    </tr>
    <tr align="center">
    <td>
    SystemCommandsOutputCode
    <td><img src="https://user-images.githubusercontent.com/75898886/231918317-77325348-1f87-4fa3-af77-c9b421f6ea24.png" width=70% height=70%> <br>
  Perintah hadoop fs -ls dijalankan menggunakan operator  disimpan dalam variabel output. Hasil dari perintah tersebut akan dicetak ke layar dengan menggunakan println. Pada Scala akan menampilkan keluaran dari command shell dan mengembalikan hasil sebagai String dalam bentuk keluaran tersebut. Dalam hal ini, variabel output akan berisi output dari perintah hadoop fs -ls.
  </td>
   </tr>
 </table>
