1.  Percobaan Antarmuka Ethernet

    Antarmuka Ethernet diidentifikasi oleh sistem dengan menggunakan model penamaan ethX dimana nilai X merepresentasikan angka urutan dimulai dari angka awal 0. Untuk melakukan konfigurasi
    antarmuka Ethernet diperlukan beberapa perangkat lunak tambahan, seperti ethtool & Ifconfig. Jika pada sistem belum ditemukan aplikasi tsb, silahkan melakukan instalasi dengan apt-get.
    
    ![image](https://github.com/user-attachments/assets/67e6df51-8b74-4c47-9cba-cd3ed05da7d3)
    * Lakukan instalasi net-tools karena belum ada net-tools pada sistem.

    ![image](https://github.com/user-attachments/assets/a8d58d65-8c2b-4c2f-9dd9-41a06a5964da)
    * Melakukan identifikasi	antarmuka	Ethernet.	Antarmuka yang menggunakan enp hanya ada satu yaitu enp0s3, dengan detail Ethernet sebagai metode enkapsulasi link, artinya 
      Antarmuka ini akan membungkus paket dalam bingkai Ethernet untuk transmisi. Serta memiliki alamat hardware 08:00:27:e3:53:25.

    ![image](https://github.com/user-attachments/assets/3845df37-4927-4c04-9a62-493f64eb57c0)
    * Perintah lshw digunakan untuk menampilkan detail antarmuka linux yang kita gunakan, mulai dari merk produk hingga kapabilitas yang dimiliki antarmuka.

    ![image](https://github.com/user-attachments/assets/a5ff6458-529d-49f9-b1bc-eb0aff1813fb)
    ![image](https://github.com/user-attachments/assets/fbddaa7a-b41f-4f09-8808-8e152abe67c5)
    * Aplikasi ethtool dapat digunakan untuk menampilkan dan mengkonfigurasi antarmuka Ethernet seperti auto-negotiation, kecepatan antarmuka Ethernet, duplex mode, dan Wake on-LAN.
    * Melakukan instalasi ethtool terlebih dahulu karena aplikasi ethtool belum ditemukan. Dan gambar tersebut aplikasi ethool telah terinstall dan siap digunakan.
      


    

      
