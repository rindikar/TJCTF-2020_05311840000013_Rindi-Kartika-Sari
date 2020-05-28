# TJCTF-2020_Login
## Description
Could you login into this [very secure site](http://login.tjctf.org/)? Best of luck! <br>
![01](https://user-images.githubusercontent.com/49342639/83090259-901ada80-a0c2-11ea-8882-33aa727f13b5.PNG)

## Solution
1. Mari kita lakukan __inspect element__ dari website ```login``` tersebut dengan klik tombol __F12__ pada keyboard dan tinjau pada bagian __Sources__ untuk ```(index)```<br>
![02](https://user-images.githubusercontent.com/49342639/83101332-4e972900-a0dc-11ea-964d-a8bcd15e1cf7.PNG)

2. Perhatikan bagian __script__ pada __head__<br>
![03](https://user-images.githubusercontent.com/49342639/83101533-bd748200-a0dc-11ea-917a-b9d8811adacb.PNG)
	<br>Terdapat sebuah model dari _success login_ yakni dengan _username_ ```admin``` dan _password_ yang masih dalam bentuk __Hash__ yang harus kita deskripsikan menggunakan _online MD5 decryptor tools_ yakni ```MD5 online```<br>	![04](https://user-images.githubusercontent.com/49342639/83101934-a5513280-a0dd-11ea-8a6e-5f86db9b23cf.PNG)

	![05](https://user-images.githubusercontent.com/49342639/83102474-c1090880-a0de-11ea-80f0-449c856ffe33.PNG)
	<br> Dan, berikut hasil deskripsinya yang akan kita gunakan sebagai _password_ <br>
	![06](https://user-images.githubusercontent.com/49342639/83102557-f4e42e00-a0de-11ea-9c64-f19bf7b4457f.PNG)

3. Kita coba melakukan _login_ kembali dengan _username_ ```admin``` dan _password_ ```inevitable```<br>
![07](https://user-images.githubusercontent.com/49342639/83102626-1e04be80-a0df-11ea-8259-9a796f3f1fc1.PNG)
	<br>Apakah flag akan didapatkan setelah memilih untuk klik tombol _login_ tersebut?<br>
	![08](https://user-images.githubusercontent.com/49342639/83102680-4391c800-a0df-11ea-891a-dfe22f9d9cfa.PNG)
	

## Flag
```html
tjctf{inevitable890898}
```
Success to login and get the flag :gift: <br>
![Solved12](https://user-images.githubusercontent.com/49342639/83102844-ac794000-a0df-11ea-8ec6-742f98172baa.PNG)
