### **Nama**      : Rijal Ammar
### **Kelas**     : TI -3B
### **Tugas**      : Pertemuan 5
# 

# Screenshot dan Penjelasan

<table>
  <tr align="center">
    <td>
    Accumulator
    <td> <img src="https://user-images.githubusercontent.com/95725937/227154198-9bc0d6b6-d351-4df0-a201-d85b6f42fe16.png" width=70% height=70%><br>
        Kode tersebut membuat sebuah variabel accumulator yang dinamakan myaccum dengan nilai awal 0 menggunakan metode sc.accumulator yang disediakan oleh SparkContext sc. Kemudian membuat sebuah RDD (Resilient Distributed Dataset) yang dinamakan myrdd dengan memparallelkan kisaran angka dari 1 hingga 99 (tidak termasuk 100). Setelah itu menerapkan operasi foreach pada setiap elemen dari RDD myrdd. Fungsi lambda yang dilewatkan ke operasi foreach menambahkan nilai dari setiap elemen ke dalam accumulator myaccum. Akhirnya, Mencetak nilai dari accumulator menggunakan metode value. Output dari kode tersebut adalah jumlah dari semua elemen dalam RDD, yang bernilai 4950.
    </td>
    </td>
    </tr>
    <tr align="center">
    <td>    
    Broadcast
    <td><img src="https://user-images.githubusercontent.com/95725937/227154393-c896915a-a461-4193-bf72-1d5cf854e493.png" width=70% height=70%><br>
  Kode tersebut membuat variabel broadcastVar dengan daftar bilangan bulat dari 1 hingga 99 menggunakan metode sc.broadcast. Metode broadcastVar.value digunakan untuk mengambil nilai variabel tersebut. Variabel tersebut didistribusikan ke setiap executor di dalam cluster menggunakan metode sc.broadcast, sehingga mengurangi overhead jaringan. Output dari kode tersebut adalah daftar bilangan bulat dari 1 hingga 99 yang dicetak menggunakan metode value.
  </td>
    </td>
    </tr>
    <tr align="center">
    <td>
    PairRDD
    <td><img src="https://user-images.githubusercontent.com/95725937/227154401-7b816658-e21d-44ba-8156-ec19e3f97f41.png" width=70% height=70%><br>
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
