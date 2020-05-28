# TJCTF-2020_Sarah Palin Fanpage
## Description
Are you a true fan of Alaska's most famous governor? Visit the [Sarah Palin fanpage](http://sarah_palin_fanpage.tjctf.org/) <br>
![01](https://user-images.githubusercontent.com/49342639/83084617-ae2d0e80-a0b3-11ea-941d-4ad00a3660f5.PNG)

## Solution
1. Pada __menu bar__ dari website [Sarah Palin fanpage](http://sarah_palin_fanpage.tjctf.org/)  terdapat sebuah ```VIP area``` yang menjadi tempat bersembunyi ```flag```<br>
![02](https://user-images.githubusercontent.com/49342639/83085212-7de66f80-a0b5-11ea-88e4-2e4b92e9e4e9.PNG)
Namun, ternyata akses yang kita lakukan terhadap ```VIP area``` __ditolak__. Agar tidak ditolak, kita harus terlebih dahulu menyukai ```Top 10 moments```. Menyukai 10 postingan tersebut bukanlah hal yang mudah untuk dilakukan sekaligus dalam satu waktu karena ada pembatasan aktivitas ```like``` sebanyak 5 postingan dalam satu waktu <br>
![03](https://user-images.githubusercontent.com/49342639/83085510-60fe6c00-a0b6-11ea-8a68-2339c6402eb0.PNG)

2. Kembali ke ```VIP area``` dan lakukan __inspect element__ dengan cara klik tombol __F12__ pada keyboard. Dan mari kita lihat ```Cookies``` pada bagian ```Application``` <br>
![04](https://user-images.githubusercontent.com/49342639/83085673-d702d300-a0b6-11ea-9964-b30b4cdc4a33.PNG)
	<br>Terdapat 3 (tiga) buah cookies. Mana yang harus kita ubah? Iya, yang harus kita ubah adalah ```value``` dari ```data``` yakni ```eyIxIjpmYWxzZSwiMiI6ZmFsc2UsIjMiOmZhbHNlLCI0IjpmYWxzZSwiNSI6ZmFsc2UsIjYiOnRydWUsIjciOnRydWUsIjgiOnRydWUsIjkiOnRydWUsIjEwIjp0cnVlfQ%3D%3D```. Apa maksud dari _value_ tersebut? 
	
3. Lakukan pendeskripsian _value_ di atas menggunakan _online decode tools_ yakni ```Base64 Decode and Encode``` <br>
![05](https://user-images.githubusercontent.com/49342639/83085941-9788b680-a0b7-11ea-9228-331915aaa625.PNG)
Hasil **_Decode_** menunjukkan 
	```html
	{"1":false,"2":false,"3":false,"4":false,"5":false,"6":true,"7":true,"8":true,"9":true,"10":true}
	``` 

4. Dikarenakan tadi kita sudah menyukai 5 postingan terbawah dari ```Top 10 moments```, maka _value_ untuk postingan __6-10__ adalah __true__. Oleh karena itu, agar kita bisa menyukai kesepuluh momen pada ```Top 10 moments``` dalam satu waktu maka kita perlu mengganti _value_ untuk postingan __1-5__ dengan __true__ pula. <br>
Kita lakukan **_Encode_** pada hasil **_Decode_** yang sudah kita ganti <br>
![06](https://user-images.githubusercontent.com/49342639/83086346-bb003100-a0b8-11ea-91ea-7831e7a7339b.PNG)
	<br> Dan berikut merupakan hasil **_Encode_**-nya
	```html
	eyIxIjp0cnVlLCIyIjp0cnVlLCIzIjp0cnVlLCI0Ijp0cnVlLCI1Ijp0cnVlLCI2Ijp0cnVlLCI3Ijp0cnVlLCI4Ijp0cnVlLCI5Ijp0cnVlLCIxMCI6dHJ1ZX0=
	```
5. Hasil **_Encode_** tersebut kita masukkan pada ```value``` dari ```data``` untuk menggantikan __value lama__ <br>
![07](https://user-images.githubusercontent.com/49342639/83086527-3661e280-a0b9-11ea-85a6-1c5204e19258.PNG)
`<br>Lakukan **_refresh_** pada halaman ```VIP area```<br>
![08](https://user-images.githubusercontent.com/49342639/83086687-a53f3b80-a0b9-11ea-9149-8d2ab7dc75e4.PNG)


## Flag
```html
tjctf{wkDd2Pi4rxiRaM5lOcLo979rru8MFqVHKdTqPBm4k3iQd8n0sWbBkOfuq9vDTGN9suZgYlH3jq6QTp3tG3EYapzsTHL7ycqRTP5Qf6rQSB33DcQaaqwQhpbuqPBm4k3iQd8n0sWbBkOf}
```
So, truly i'm your biggest fan :wink: <br>
![Solved13](https://user-images.githubusercontent.com/49342639/83086792-ee8f8b00-a0b9-11ea-937e-2912482fbcc8.PNG)
