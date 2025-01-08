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

2. Mematikan dan Mengaktifkan antarmuka Ethernet
   Antarmuka Ethernet dapat dimatikan dan diaktifkan dengan menggunakan perintah ifdown dan ifup.
        Mematikan antarmuka Ethernet dengan perintah:
            $ sudo ifdown enp0s3
        Mengaktifkan antarmuka Ethernet dengan perintah:
            $ sudo ifup enp0s3
   ![image](https://github.com/user-attachments/assets/e9dafaec-7bd2-4382-a9ef-9e24e21d191e)
   ![image](https://github.com/user-attachments/assets/0df34240-abc9-4080-a1c0-5076028d0712)
   ![image](https://github.com/user-attachments/assets/7218e732-f8de-4610-a351-c264b6cbe1ba)
   * terlebih dahulu melakukan instalasi ifupdown.
   ![image](https://github.com/user-attachments/assets/d670311b-f0e8-47c3-9b6b-ece9046d1c57)
   * Perintah "sudo ifdown enp0s3" diatas digunakan untuk mematikan interface enp0s3, artinya transmisi koneksi ke jaringan kita telah dimatikan.
   ![image](https://github.com/user-attachments/assets/620317b5-db50-425b-b699-793d6a1d7760)
   * Mengecek apakah enp0s3 telah dimatikan.
   ![image](https://github.com/user-attachments/assets/dc48bbac-dfb6-46d7-863c-d6ead5f836a9)
   * Perintah "sudo ifup enp0s3" diatas digunakan untuk menyalakan kembali interface enp0s3 dengan detail DHCP yang telah diberikan oleh jaringan.
   ![image](https://github.com/user-attachments/assets/8e22d70b-9daf-4e24-bec5-c75d3666d2b2)
   * Melakukan pengecekan apakah enp0s3 telah nyala kembali.

3. Menampilkan driver antarmuka Ethernet
   ![image](https://github.com/user-attachments/assets/cb4c916d-aa66-4f16-b76d-85519cc33603)
   * Perintah diatas pada gambar digunakan untuk menampilkan driver antarmuka Ethernet. Driver yang digunakan adalah e1000 dengan versi 7.3.21-k8-NAPI.
4. Menampilkan satistik jaringan pada antarmuka Ethernet
   ![image](https://github.com/user-attachments/assets/701ac7c0-2f0e-40e5-8d93-abc00fc2f3c5)
   ![image](https://github.com/user-attachments/assets/cbe47e62-1948-484a-b165-dbc7a0f654be)
   ![image](https://github.com/user-attachments/assets/30b480b3-cf2e-4ab6-a36f-cafe6aa240bf)
   * Perintah diatas pada gambar digunakan untuk menampilkan statistik jaringan pada antarmuka Ethernet dari enp0s3 dengan detail seperti gambar diatas yang berisi paket-paket yang telah 
     dilewati antarmuka enp0s3.
   * Penjelasan  masing-masing atribut yang terdapat pada statistik yang telah didapatkan :
        rx_packets	: jumlah paket yang telah diterima
        tx_packets	: jumlah paket yang telah dikirimkan
        rx_bytes	: jumlah byte data yang telah diterima
        tx_bytes	: jumlah byte data yang telah dikirimkan
        rx_broadcast	: paket broadcast yang diterima
        tx_broadcast	: paket broadcast yang dikirimkan
        rx_multicast	: jumlah paket multicast(group) diterima
         tx_multicast	: jumlah paket multicast(group) dikirimkan
         rx_errors	: jumlah error diterima
         tx_errors	: jumlah error dikirimkan
         tx_dropped	: jumlah paket drop yang dikirimkan
         multicast	: packet group atau sekumpulan
         collisions	: jumlah tabrakan paket.

5. PENGALAMATAN IP & DNS
   A. Percobaan Pengalamatan IP
      Percobaan tersebut dilakukan untuk melakukan konfigurasi alamat IP pada sistem dan default gateway agar sistem dapat berkomunikasi pada jaringan area lokal maupun Internet.
      a. Konfigurasi IP address sementara
         ![image](https://github.com/user-attachments/assets/cd6a4b41-54f7-40d7-9c06-8220ab221110)
         * Melakukan konfigurasi alamat IP antarmuka jaringan enp0s3, dengan detail :
            IP Address	: 192.168.56.29
            Netmask	    : 255.255.255.0
       b. Verifikasi konfigurasi alamat IP
          ![image](https://github.com/user-attachments/assets/77575a9b-c919-4d1b-990d-48df78da87b8)
          * Tampilan detail antarmuka enp0s3 yang telah dilakukan konfigurasi IP Address sebelumnya.
       c. Konfigurasi default gateway
          Untuk melakukan konfigurasi gateway, dapat menggunakan perintah route dan melakukan konfigurasi alamat gateway sesuai dengan kebutuhan jaringan yang diinginkan.
          ![image](https://github.com/user-attachments/assets/89d29425-6467-4444-ba1d-79e5ae07006c)
          * Melakukan konfigurasi default gateway pada enp0s3 dengan IP 192.168.56.110
       d. Verifikasi konfigurasi default gateway
          ![image](https://github.com/user-attachments/assets/2c41afee-07ad-4cdc-acc3-a162cb82b9c7)
          * Menampilkan default gateway yang ada pada antarmuka jaringan. Penambahan default gateway sebelumnya berhasil dilakukan ditandai dengan masuknya gateway tambahan pada daftar 
            yaitu 192.168.56.110
       e. Konfigurasi Dynamic IP Address Assignment
          ![image](https://github.com/user-attachments/assets/d4dcf615-8f13-47fd-85cc-25ba08e13603)
          ![image](https://github.com/user-attachments/assets/505ddb47-984d-4325-95cd-efd1c657d060)
          * Lakukan konfigurasi interface pada enp0s3 menjadi dhcp.
          ![image](https://github.com/user-attachments/assets/e6d6f2be-0bee-40eb-a043-028d18e24795)
          * Melakukan pengecekan bahwa Antarmuka enp0s3 telah terkonfigurasi dan aktif.
       f. Konfigurasi alamat IP 
          ![image](https://github.com/user-attachments/assets/ac2cdb4a-84d5-4236-964c-95734e7c75dd)
          ![image](https://github.com/user-attachments/assets/8d1dad80-fa70-451b-9cd9-6771ca880dd5)
          * Lakukan konfigurasi IP static pada antarmuka enp0s8, dengan detail :
                   IP Address	: 10.25.1.2
                   Netmask	: 255.255.255.0
                   Gateway	: 10.25.1.1
          ![image](https://github.com/user-attachments/assets/0867ad6a-fad8-4d3f-8b34-3bfbb2615e31)
          * Mengaktifkan kembali enp0s3 dengan ifup kemudian antarmuka enp0s3 sudah terkonfigurasi sesuai dengan konfigurasi yang dilakukan sebelumnya. 

   













      


    

      
