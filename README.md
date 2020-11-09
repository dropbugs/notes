# Prinsip *Clean Code*: Menjadi lebih baik

### Aturan:
* **Gunakan nama yang mudah diucapkan untuk *variables* dan *methods***, Jangan gunakan singkatan dalam nama *variables* dan *methods*. 
  Gunakan nama *variable* dalam bentuk lengkap agar mudah diucapkan dan/atau semua orang bisa memahaminya.
  ```kotlin
  #1
  ✖ val addCmt
  ✔ val addComment 
  
  #2
  ✖ for(x in people) {}
  ✔ for(person in people) {}
  
  #3
  ✖ user.createUser() // redudansi
  ✔ user.create()
  ```
  
* **Gunakan nama sesuai tujuan**, Tujuan *variable* harus dapat dimengerti oleh seseorang yang membaca nama *variable* tersebut.
  ```kotlin
  #1
  ✖ val d // elapsed time in days
  ✔ val elapsedTimeInDays, val daySinceCreation,s val fileAgeInDays 

  #2
  ✖ if ("paid" == application.status) {}
  ✔ if (application.isPaid) {}
  ```
  
* **Jangan terlalu berinovasi, be simple!**. Tunjukan inovasi dalam logika 👌, bukan dalam penamaan *variables* atau *methods*.
  ```kotlin
  #1
  ✖ order->letItGo()
  ✔ order->delete()
  ```
  
* **Konsisten**, Gunakan satu kata untuk yang serupa. Jangan gunakan "*fetch*" di satu *Class* dan "*get*" di *Class* lain.

* **Jangan ragu untuk menggunakan istilah teknis dalam penamaan**, Silakan gunakan istilah teknis. Misalnya, *jobQueue* lebih baik daripada *jobs*
  
* **Gunakan kata kerja(*verb*) sebagai awalan dalam penulisan *method* dan gunakan kata benda(*noun*) untutk *Class***, Gunakan gaya penulisan *camelCase* untuk semua *variables* dan *methods*. Untuk penamaan *Class* harus diawali dengan kapital.
  ```kotlin
  #1
  ✖ fun priceIncrement() {}
  ✔ fun incrementPrice() {}
  
  #2
  ✖ var lengthValidateSubDomain
  ✔ var validateLenghtOfSubDomain
  
  #3
  ✖ class calculationIncentive() {}
  ✔ class Incentive() {}
  ```
  
* **Gunakan konvensi penamaan yang konsisten**, Selalu gunakan huruf kapital, dan pisahkan kata dengan ``_`` (Underscore)
  ```kotlin
  const val SECRET_KEY = "12345678"
  ```

* **Buat fungsi yang jelas**, Buatlah fungsi sesingkat mungkin. Panjang metode ideal -/+ 15 baris. Terkadang bisa lebih panjang, tapi kodenya kalau bisa harus *clean* secara konseptual untuk dipahami.

* **Pertahankan Parameter/Argumen kurang dari satu atau paling banyak 3**, Jika argumen lebih besar dari tiga, maka harus berpikir untuk me-**refactor** fungsi menjadi *Class* 

> Biasakan membatasi *function/method* untuk satu tugas. Hindari menggunakan "**dan**" dalam nama *method*, seperti "**validateAndSave**". 
> Sebagai gantinya, buat dua method. Satu untuk validasi dan satu lagi untuk menyimpan.

* **Perilaku *Class* dan *Objet***, Satu *Class* harus melakukan satu hal. 

* **Jangan mengomentari kode yang buruk**, Beri komentar hanya jika diwajibkan secara hukum atau jika Anda perlu membuat catatan tentang masa depan atau riwayat program.
  ```kotlin
  #1
  Check to see if the employee is eligible for full benefits
  ✖ if (employee->flag && self::HOURLY_FLAGS && employee.age > 45) {}
  ✔ 
  ```
  
* **Gunakan Git/Subervesion untuk mengontrol riwayat *project*** *

* **Hindari Array Jumbo** 

* **Jangan mengulang code** *

* **Don't Hardcode** *

