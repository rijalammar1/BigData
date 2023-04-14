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
        Kode tersebut membuat sebuah variabel accumulator yang dinamakan myaccum dengan nilai awal 0 menggunakan metode sc.accumulator yang disediakan oleh SparkContext sc. Kemudian membuat sebuah RDD (Resilient Distributed Dataset) yang dinamakan myrdd dengan memparallelkan kisaran angka dari 1 hingga 99 (tidak termasuk 100). Fungsi lambda yang dilewatkan ke operasi foreach menambahkan nilai dari setiap elemen ke dalam accumulator myaccum. Akhirnya, Mencetak nilai dari accumulator menggunakan metode value. Output dari kode tersebut adalah jumlah dari semua elemen dalam RDD, yang bernilai 4950.
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
      Kode tersebut membuat sebuah RDD bernama myRDD dengan tiga elemen menggunakan metode parallelize dari SparkContext sc. Selanjutnya, sebuah Pair RDD dengan nama myPairRDD dibuat dari myRDD dengan menggunakan metode map. Fungsi lambda yang dilewatkan ke metode map akan mengembalikan tuple yang terdiri dari elemen RDD dan panjangnya. Metode collect digunakan untuk mencetak tuple dari setiap elemen dalam RDD myPairRDD. Selain itu, metode keys digunakan untuk mengambil semua kunci dari setiap tuple dalam RDD myPairRDD, dan metode values digunakan untuk mengambil semua nilai dari setiap tuple dalam RDD myPairRDD. Output dari kode tersebut adalah sebuah tuple yang terdiri dari elemen RDD dan panjangnya, serta dua buah daftar yang masing-masing berisi kunci dan nilai dari setiap tuple dalam RDD myPairRDD.
  </td>
    </td>
    </tr>
    <tr align="center">
    <td>
    WordCount
    <td>
      <img src="https://user-images.githubusercontent.com/95725937/227154712-aae7c89b-8240-4850-b369-4407c315bb0b.png" width=70% height=70%>
      <img src="https://user-images.githubusercontent.com/95725937/227154745-a9869069-51da-48c7-aed3-b0dae5d12bc2.png" width=70% height=70%><br>
      Pertama, kode membaca file README.md menggunakan metode textFile dari SparkContext sc. Selanjutnya, teks dalam file tersebut dibagi menjadi kata-kata dengan menggunakan fungsi split pada setiap baris teks melalui metode flatMap. Setiap kata dalam RDD tersebut akan dibuat menjadi tuple dengan nilai awal 1 melalui fungsi map. Setiap tuple dengan kata yang sama akan dijumlahkan melalui metode reduceByKey dengan menggunakan fungsi add untuk menjumlahkan nilai. Hal ini dilakukan untuk melakukan penghitungan kata yang serupa dalam file. Hasil penghitungan jumlah kemunculan kata-kata disimpan dalam variabel output menggunakan metode collect, dan kemudian dicetak ke layar menggunakan for loop untuk mengiterasi setiap kata dan jumlah kemunculan dalam variabel output. Jumlah kemunculan kata dicetak dengan format "kata: jumlah".
  </td>
    </td>
        </tr>
    <tr align="center">
    <td>
    LogAnalytics
         <td>      
      <img src="https://user-images.githubusercontent.com/95725937/229344529-729a313b-8224-4c0e-8618-c8d309d40d13.png" width=70% height=70%><br>
           
  </td>
    </td>    
    </tr>
        <tr align="center">
    <td>
    UnderstandingRDD
         <td>      
      <img src="https://user-images.githubusercontent.com/95725937/229346307-64ae438f-2dcd-4cc0-b603-53b9a1eb9ee0.png" width=70% height=70%><br>
           
  </td>
    </td>    
    </tr>
    <tr align="center">
    <td>
    SystemCommandsReturnCode
         <td>
      <img src="https://user-images.githubusercontent.com/95725937/227154750-cac14af7-38f3-4299-a129-af5fc647b84d.png" width=70% height=70%>
      <img src="https://user-images.githubusercontent.com/95725937/227154756-ac2e8841-1026-4fc9-92ea-dd7dbf2a0018.png" width=70% height=70%><br>
           Pada baris pertama, digunakan import sys.process._ untuk mengimport library sys.process. Selanjutnya, perintah ls /tmp dijalankan menggunakan ! operator dan disimpan dalam variabel res. Hasil dari perintah tersebut akan dicetak ke layar dengan menggunakan println. Jika perintah berhasil dijalankan, maka nilai variabel res akan sama dengan 0, jika tidak berhasil maka nilai variabel res akan bernilai non-zero.
  </td>
    </td>    
    </tr>
    <tr align="center">
    <td>
    SystemCommandsOutputCode
    <td><img src="https://user-images.githubusercontent.com/95725937/227155533-dab87547-c883-4fa5-a191-0cc1f191dc7c.png" width=70% height=70%> <br>
  Pada baris pertama, digunakan import sys.process._ untuk mengimport library sys.process. Selanjutnya, perintah hadoop fs -ls dijalankan menggunakan !! operator dan disimpan dalam variabel output. Hasil dari perintah tersebut akan dicetak ke layar dengan menggunakan println. Operator !! pada Scala akan menampilkan keluaran dari command shell dan mengembalikan hasil sebagai String dalam bentuk keluaran tersebut. Dalam hal ini, variabel output akan berisi output dari perintah hadoop fs -ls.
  </td>
   </tr>
 </table>
