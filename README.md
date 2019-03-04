Automation Script for any cluster machine - Edisi Bahasa Indonesia

Script ini didesain di kluster Raspberry Pi, namun seharusnya bisa dideploy di sistem x86 Debian seperti Ubuntu. Untuk sistem CentOS / Fedora akan butuh sedikit penyesuaian namun tidak banyak. 

Script ini juga didesain untuk bisa dijalankan di kluster apapun dengan jumlah node yang scalable hingga berapapun. Script ini mengikuti aturan kluster master - slave. Kluster harus mengikuti aturan nama hostname dengan index seperti 'node1, node2, node3, node4, dtc'. User yang menggunakan script ini harus mengedit variabel 'basename','masternode','bawah', dan 'atas'.

Contoh, ketika ada kluster 8 node dengan nama 'mycluster1 - mycluster8'. Variabel basename=mycluster; masternode=${basename}1; bawah=2; atas=8
 
adduser           : Menambah user baru di semua node
deluser           : Menghapus user di semua node
passwordless-ssh  : Setting passwordless ssh pada semua node
poweroff          : Shutdown semua node
reboot            : Reboot semua node
run-command-all   : Menjalankan command pada semua node
run-command-slave : Menjalankan command pada node slave saja
testcommand       : Untuk eksperimen script baru
