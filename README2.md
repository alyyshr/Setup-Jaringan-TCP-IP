5. PENGALAMATAN IP & DNS
   
   Percobaan Pengalamatan IP
      Percobaan tersebut dilakukan untuk melakukan konfigurasi alamat IP pada sistem dan default gateway agar sistem dapat berkomunikasi        pada jaringan area lokal maupun Internet.
      Konfigurasi IP address sementara
         ![image](https://github.com/user-attachments/assets/cd6a4b41-54f7-40d7-9c06-8220ab221110)
         * Melakukan konfigurasi alamat IP antarmuka jaringan enp0s3, dengan detail :
            IP Address	: 192.168.56.29
            Netmask	    : 255.255.255.0
   
      Verifikasi konfigurasi alamat IP
          ![image](https://github.com/user-attachments/assets/f6d78420-5a09-4cf9-a521-94575ff7f16d)
          * Tampilan detail antarmuka enp0s3 yang telah dilakukan konfigurasi IP Address sebelumnya.
   
      Konfigurasi default gateway
          Untuk melakukan konfigurasi gateway, dapat menggunakan perintah route dan melakukan konfigurasi alamat gateway sesuai dengan 
          kebutuhan jaringan yang diinginkan.
          ![image](https://github.com/user-attachments/assets/89d29425-6467-4444-ba1d-79e5ae07006c)
          * Melakukan konfigurasi default gateway pada enp0s3 dengan IP 192.168.56.110
   
      Verifikasi konfigurasi default gateway
          ![image](https://github.com/user-attachments/assets/2c41afee-07ad-4cdc-acc3-a162cb82b9c7)
          * Menampilkan default gateway yang ada pada antarmuka jaringan. Penambahan default gateway sebelumnya berhasil dilakukan 
            ditandai dengan masuknya gateway tambahan pada daftar 
            yaitu 192.168.56.110
   
      Konfigurasi Dynamic IP Address Assignment
          ![image](https://github.com/user-attachments/assets/d4dcf615-8f13-47fd-85cc-25ba08e13603)
          ![image](https://github.com/user-attachments/assets/505ddb47-984d-4325-95cd-efd1c657d060)
   
          * Lakukan konfigurasi interface pada enp0s3 menjadi dhcp.

   ![image](https://github.com/user-attachments/assets/e6d6f2be-0bee-40eb-a043-028d18e24795)
          * Melakukan pengecekan bahwa Antarmuka enp0s3 telah terkonfigurasi dan aktif.
   
      Konfigurasi alamat IP 
          ![image](https://github.com/user-attachments/assets/ac2cdb4a-84d5-4236-964c-95734e7c75dd)
          ![image](https://github.com/user-attachments/assets/8d1dad80-fa70-451b-9cd9-6771ca880dd5)
          * Lakukan konfigurasi IP static pada antarmuka enp0s8, dengan detail :
                   IP Address	: 10.25.1.2
                   Netmask	: 255.255.255.0
                   Gateway	: 10.25.1.1
   
          ![image](https://github.com/user-attachments/assets/0867ad6a-fad8-4d3f-8b34-3bfbb2615e31)
          * Mengaktifkan kembali enp0s3 dengan ifup kemudian antarmuka enp0s3 sudah terkonfigurasi sesuai dengan konfigurasi yang    
            dilakukan sebelumnya. 
