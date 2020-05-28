# TJCTF-2020_Tap Dancing
## Description
My friend is trying to teach me to dance, but I am not rhythmically coordinated! They sent me a list of  [dance moves](https://static.tjctf.org/518d6851c71c5482dbd5bbe812b678684238c8f4e9e9b3d95a188f7db83a0870_cipher.txt)  but they're all numbers! Can you help me figure out what they mean so I can learn the dance?

__NOTE__: Flag is not in flag format.

## Solution
1. **_List of dance moves_** yakni sebagai berikut: <br>
```1101111102120222020120111110101222022221022202022211```

2. Makna dibalik deretan angka tersebut ialah **_Morse Code_**, sehingga kita harus mengubahnya menjadi **_Morse Code_** dengan kunci berikut: <br>
	```html
	1 diganti dengan (tanda minus) -
	2 diganti dengan (tanda titik) .
	0 diganti dengan (spasi)
	```
	Sehingga didapatkanlah **_Morse Code_** seperti ini:<br>
	```-- ----- .-. ... . -. ----- - -... ....- ... . ...--```

3. **_Morse Code_** tersebut dideskripsikan menggunakan _online morse decoder_ yakni ```Morse Code Translator``` untuk mendapatkan ```flag```<br>
![02](https://user-images.githubusercontent.com/49342639/83119571-156db180-a0fa-11ea-9b62-4b921bd69cd9.PNG)

## Flag
```html
M0RSEN0TB4SE3
```
The different one of the flag :mag:<br>
![Solve10](https://user-images.githubusercontent.com/49342639/83119872-75645800-a0fa-11ea-8e52-0e28a005816b.PNG)
