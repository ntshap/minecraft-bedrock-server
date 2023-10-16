# Minecraft Bedrock Server di Ubuntu Server 20.04
Panduan ini akan membantu Anda menginstal dan menjalankan server Minecraft Bedrock Edition pada Ubuntu Server 20.04. Pastikan Anda telah mengakses server Anda melalui SSH sebelum memulai.
# minimum spesifikasi server yang di perlukan
- 1 CPU
- 2 GB RAM
- 20 GB Storage
- Fast Internet Connection
- Have a IP Public
# Masuk via SSH
masuk ke server Anda melalui SSH. bisa menggunakan software putty lalu memasukkan IP Host name (IP address) yang terdapat pada ubuntu server
# Membuat user baru
```
adduser minecraft
```
``` 
usermod -aG sudo minecraft
```
# Masuk ke user yang sudah dibuat
``` 
su - minecraft
```
# Install Java, Screen, Wget, Unzip #
``` 
sudo apt update -y
```
``` 
sudo apt install openjdk-8-jdk -y
```
``` 
sudo apt install screen -y
```
``` 
sudo apt install wget -y
```
``` 
sudo apt install unzip -y
```
# Buka port server #
``` 
sudo ufw enable
```
``` 
sudo ufw allow 22/tcp
```
``` 
sudo ufw allow 80/tcp
```
``` 
sudo ufw allow 19132/tcp
```
``` 
sudo ufw allow 19132
```
``` 
sudo ufw allow 25565/tcp
```
# Install dan jalankan Minecraft Server #
``` 
cd /home/minecraft
```
``` 
wget https://minecraft.azureedge.net/bin-linux/bedrock-server-1.17.41.01.zip
```
``` 
unzip bedrock-server-1.17.41.01.zip
```
``` 
chmod +x ./bedrock_server
```
``` 
sudo ./bedrock_server
```
![Screenshot_2023-10-16-11-57-33-638_com mojang minecraftpe](https://github.com/ntshap/minecraft-bedrock-server/assets/145199476/208593dd-79cf-438e-8d94-996e940e47d8)

# Jika ingin menjalankan server di background, ketik perintah ini #
``` 
sudo nohup ./bedrock_server &
```
# Jika kamu ingin melihat prosesnya, kamu bisa ketik perintah ini #
``` 
htop
```
