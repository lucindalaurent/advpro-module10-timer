## Tutorial 1: Timer
### 1.2. Understanding how it works.
#### The modification
![modication in main](documentation/heyhey.png)
#### The execution
![execution 1.2](documentation/heyheyprint.png)
#### The explanation
Pada kode di atas, saya melakukan modifikasi dengan menambahkan _task_ untuk mencetak "hey hey". _Task_ tersebut berada di luar _task_ yang di-_spawn_ dalam `spawner.spawn(...);`. _Task_ yang berada di dalam `spawner.spawn(...);` akan dijalankan secara asinkronus, "terpisah" dari main program. Oleh karena itu, _task_ untuk mencetak "hey hey" dapat dijalankan terlebih dahulu. Dengan kata lain, program tidak perlu menunggu _task_ yang berada di dalam `spawner.spawn(...);` selesai dijalankan untuk menjalankan _task_ lain di main. Adapun _task_ yang berada di dalam `spawner.spawn(...);` adalah mencetak "howdy", kemudian menunggu selama 2 detik menggunakan `TimerFuture` dan terakhir mencetak "done!". Hasil eksekusinya seperti tampak pada gambar: program mencetak "hey hey", mencetak "howdy", menunggu 2 detik, kemudian mencetak "done!".