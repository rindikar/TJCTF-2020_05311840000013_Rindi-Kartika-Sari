# TJCTF-2020_Gamer W
## Description
Can you figure out how to [cheat](http://gamer_w.tjctf.org/) the system? Grab his hat to prove your victory!

## Solution
1.  Untuk memainkan, ada beberapa aplikasi yang digunakan. Kali ini menggunakan  [Chrome Extension Cetus](https://github.com/Qwokka/Cetus). Cetus digunakan untuk memanipulas.
2.  Masuklah ke dalam __shop__ dan mulai untuk melakukan aktivitas __manipulasi__
3.  Manipulasi yang pertama adalah memodifikasi value dari gold sendiri. Search menggunakan Cetus dengan  `comparison operator EQ`  dan  `value type f32`<br>
	<img width="358" alt="01" src="https://user-images.githubusercontent.com/49342639/83147909-78733e80-a122-11ea-9b78-8f3c1abb8717.png">
4. Dan akan ditemukan __kode untuk gold__ yakni```0x02111f3c```
5.  Bookmark dan ubah __value gold__ sebanyak mungkin untuk membeli semua item yang ada di __shop__
6.  ```Level 1``` hanya melawan monster hijau (dapat dikerjakan __tanpa melakukan cheat__)<br>
	<img width="691" alt="02" src="https://user-images.githubusercontent.com/49342639/83148289-fa636780-a122-11ea-8091-22c6fb0f9337.png">
7. ```Level 2``` akan melawan 3 monster hijau yang sama dengan level 1 (dapata dikerjakan __tanpa melakukan cheat__)<br>
	<img width="687" alt="03" src="https://user-images.githubusercontent.com/49342639/83148487-38f92200-a123-11ea-9e42-8a4006c0078b.png">
8. ```Level 3``` akan memunculkan __bos__ pemilik monster monster tersebut (dapat dikerjakan __tanpa  melakukan cheat__)<br>
	<img width="691" alt="04" src="https://user-images.githubusercontent.com/49342639/83148792-92f9e780-a123-11ea-83dc-0f772df88c00.png">
9. ```Level 4``` __bos__ tersebut akan ter-upgrade dan memiliki _machine gun_ yang dapat menembak banyak peluru hijau sekaligus (sehingga kita __harus melakukan cheat__)<br>
	<img width="688" alt="05" src="https://user-images.githubusercontent.com/49342639/83148970-c50b4980-a123-11ea-8ebb-5e27b92919fb.png">
10. Dengan menggunakan Cetus, ubah total hp dari pemain (kita/user). Kode untuk hp pemain adalah ```0x2112f1c```
11.  Bookmark dan ubah valuenya menjadi banyak supaya tidak mati-mati saat terkena tembakan hijau.  
12.  ```Level 5``` __bos__ akan minum potion yang membuat lifenya regenerate jika terkena serangan (menggunakan cheat untuk ubah __hp bos__)
13.  __Bos__ tersebut memiliki hp  `300`  (diketahui dengan cara menghitung  😏). Kode untuk __hp bos__ yakni:<br>
		```
		0x2112e4c
		```<br>
14.  Bookmark, freeze, dan ubah valuenya menjadi ```0```<br>
15.  Win win chicken dinner! 

## Flag
```html
tjctf{c3tus_del3tus_ur_m3ms_g0ne}
```
Win the game :game_die:<br>
![Solve20](https://user-images.githubusercontent.com/49342639/83149501-5d093300-a124-11ea-80cd-cbb5092d04ca.PNG)
