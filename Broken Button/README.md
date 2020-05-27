# TJCTF-2020_Broken Button
## Description
This [site](http://broken_button.tjctf.org/) is telling me all I need to do is click a button to find the flag! Is it really that easy?

## Solution
1. Mari kita kunjungi terlebih dahulu [site](http://broken_button.tjctf.org/) <br>
![01](https://user-images.githubusercontent.com/49342639/83020696-0ed82f00-a053-11ea-9f11-b930cb09a571.PNG)

2. Dari website tersebut, lakukan pengecekan pada ```inspect element``` dengan klik tombol ```F12``` pada keyboard <br>
![02](https://user-images.githubusercontent.com/49342639/83021048-9887fc80-a053-11ea-8ea7-f68de729c9b2.PNG)

3. Perhatikan bagian ```body```  dan dapat kita lihat ada bagian ```body``` yang tertutup <br>
![03](https://user-images.githubusercontent.com/49342639/83021311-03393800-a054-11ea-9270-7bd579189508.PNG)
	
	<br>Bukalah bagian ```body``` yang tertutup tersebut <br>
![04](https://user-images.githubusercontent.com/49342639/83021502-4abfc400-a054-11ea-8a4c-830701e7c015.PNG)
	<br> Pada bagian ```button class``` terdapat arahan untuk menuju suatu **_link_** ketika kita melakukan klik pada ```button``` <br>
	```html
	<button class="hidden" href="find_the_flag!.html"></button>
	```
4. Tambahkan __arahan link__ tersebut ke dalam **_Address bar_** dari __link utama website__<br>
![05](https://user-images.githubusercontent.com/49342639/83022192-56f85100-a055-11ea-99d9-4e1085d32403.PNG)

	<br> Dan, mari kita lihat hasilnya :eyes: <br>
	![06](https://user-images.githubusercontent.com/49342639/83022361-9f177380-a055-11ea-8561-d0d3b23e69c8.PNG)

## Flag
```html
tjctf{wHa1_A_Gr8_1nsp3ct0r!}
```
Flag always give me a point :clap: <br>
![Solved3](https://user-images.githubusercontent.com/49342639/83022708-1fd66f80-a056-11ea-97c3-c6d472f580c7.PNG)
