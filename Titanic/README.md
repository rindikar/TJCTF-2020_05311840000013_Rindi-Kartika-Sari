# TJCTF-2020_Titanic
## Description
I wrapped tjctf{} around the lowercase version of a word said in the 1997 film "Titanic" and created an MD5 hash of it: ```9326ea0931baf5786cde7f280f965ebb```

## Solution
```Flag``` akan berbentuk ```tjctf{sebuah kata yang diucapkan dalam film Titanic}```. Sebuah kata tersebut dibungkus dalam ```tjctf{}``` dalam bentuk _lowercase_.<br>
1. Unduh _script_ untuk film [Titanic](https://loadsubs.net/movies2/files/titanic-en1.srt)
2. Dalam _script_ terdapat banyak karakter ```.``` ```,``` ```:``` dan ```/```, maka 4 (empat) karakter tersebut harus kita __hapus__. Sedangkan, untuk setiap ```spasi``` diganti menjadi __enter__ sehingga akan terbentuk satu kata per baris. <br>
3. Setiap kata per baris dibungkus dengan ```tjctf{}``` <br>
	![01](https://user-images.githubusercontent.com/49342639/83083589-b899d900-a0b0-11ea-8921-73adcc1de688.PNG)
	
4. Pada **_Description_** terdapat __MD5 Hash__ dari ```flag yang dicari```. Oleh karena itu, setiap kata yang telah dibungkus dengan ```tjctf{}``` dilakukan **_hashing_** menggunakan __MD5__ melalui _online hashing tools_ yakni ```MD5 Hash Generator```<br>
![02](https://user-images.githubusercontent.com/49342639/83083848-72914500-a0b1-11ea-934f-35c26b856c92.PNG)

5. Akhirnya ditemukan satu kata dari _script_ yang memiliki _MD5 Hash_ yang sama dengan yang telah dideklarasikan pada **_Description_**<br>
![03](https://user-images.githubusercontent.com/49342639/83084052-0ebb4c00-a0b2-11ea-953d-5c0260ff0662.PNG)

## Flag
```html
tjctf{marlborough's}
```
It is take too much time to find it but all the struggle paid by the point :clock11: <br>
![Solved14](https://user-images.githubusercontent.com/49342639/83084265-aae55300-a0b2-11ea-93d9-7cd0b1de425f.PNG)
