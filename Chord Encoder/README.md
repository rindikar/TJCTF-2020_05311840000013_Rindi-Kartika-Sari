# TJCTF-2020_Chord Encoder
## Description
I tried creating my own  [chords](https://static.tjctf.org/67be5bd036a4be8323314d1da6ad2e673963f76634a62ec47d53fb07a04a3722_chords.txt), but my  [encoded sheet music](https://static.tjctf.org/c29857b8d4d1b2dfe502b5053d73844a08358ae681b2af8de6829b765dc2c28e_notes.txt)  is a little hard to read. Please play me my song! <br>
[chord_encoder.py](https://static.tjctf.org/da36df431da358250884ff9765e8c0c5f054b845aff31b85e37229159176bb9f_chord_encoder.py) <br>
__Hint__: ```Pathfinding? I just need some sick jams B)```

## Solution
1. Lakukan pengonversian isi dari file __encoded sheet music__ ke dalam bentuk suatu file bereksistensi ```.txt```<br>
__Isi dari file encoded sheet music__ :<br>
```1121112111211002112101121121001001210000101221121011200102000110120200101100100111211011001020020010111012011202001011112110121121011211211002112110020200101111210112020010111121010112102001121100211211011020020001010``` <br>
__Hasil konversi ke dalam bentuk file__ ```.txt```:<br>
	```html
	1121
	1121
	1121
	1002
	1121
	0112
	1121
	001
	001
	2100
	001
	0122
	1121
	0112
	001
	020
	001
	1012
	0200
	1011
	001
	001
	1121
	1011
	001
	020
	0200
	1011
	1012
	0112
	0200
	1011
	1121
	1012
	1121
	0112
	1121
	1002
	1121
	1002
	0200
	1011
	1121
	0112
	0200
	1011
	1121
	0200
	1121
	0200
	1121
	1002
	1121
	1011
	020
	020
	001
	010
	```

2. Lakukan pengonversian kembali dari hasil konversi langkah pertama berdasarkan file __chords.txt__ (di bawah ini) menjadi hasil konversi kedua:<br>
	```html
	A 0112
	B 2110
	C 1012
	D 020
	E 0200
	F 1121
	G 001
	a 0122
	b 2100
	c 1002
	d 010
	e 0100
	f 1011
	g 000
	```
	<br>__Hasil konversi kedua berdasarkan file ```chord.txt``` di atas__:<br>
	```html
	F
	F
	F
	c
	F
	A
	F
	G
	G
	b
	G
	a
	F
	A
	G
	D
	G
	C
	E
	f
	G
	G
	F
	f
	G
	D
	E
	f
	C
	1
	5
	f
	F
	C
	F
	A
	F
	c
	6
	c
	E
	f
	F
	A
	E
	f
	F
	d
	F
	E
	F
	c
	F
	f
	D
	D
	G
	d
	```

3. Setelah kedua langkah pengonversian selesai, kita jalankan ```chord_encoder.py```<br>
```python
f = open('song1.txt').read()
l = {'1':'A', '2':'B', '3':'C', '4':'D', '5':'E', '6':'F', '7':'G'}
chords = {}
for i in open('chords.txt').readlines():
c, n = i.strip().split()
chords[c] = n
s = ''
for i in f:
c1, c2 = hex(ord(i))[2:]
if c1 in l:
c1 = l[c1]
if c2 in l:
c2 = l[c2]
s += chords[c1] + chords[c2]
open('notes.txt', 'w').write(s)
```

## Flag
```html
flag{zats_wot_1_call_a_meloD}
```
music melody give me a big energy to get the point :crescent_moon:<br>
![Solve15](https://user-images.githubusercontent.com/49342639/83145974-cdfa1c00-a11f-11ea-9329-e95b3a9edec5.PNG)
