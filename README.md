# Prinsip *Clean Code*: Menjadi lebih baik

### Aturan:
* **Gunakan nama yang mudah diucapkan untuk *variables* dan *methods***

  Jangan gunakan singkatan dalam nama *variables* dan *methods*. Gunakan nama *variable* dalam bentuk
  lengkap agar mudah diucapkan dan/atau semua orang bisa memahaminya.
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
  
* **Gunakan nama sesuai tujuan**
  
  Tujuan *variable* harus dapat dimengerti oleh seseorang yang membaca nama *variable* tersebut.
  ```kotlin
    #1
    ✖ val d // elapsed time in days
    ✔ val elapsedTimeInDays, val daySinceCreation,s val fileAgeInDays 
    
    #2
    ✖ if ("paid" == application.status) {}
    ✔ if (application.isPaid) {}
    ```
* **Jangan terlalu berinovasi, dibikin simpel aja**
  
  Tunjukan inovasi dalam logika 👌, bukan dalam penamaan *variables* atau *methods*
  ```kotlin
    #1
    ✖ order->letItGo()
    ✔ order->delete()
  ```
