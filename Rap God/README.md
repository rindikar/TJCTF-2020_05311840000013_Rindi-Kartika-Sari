# TJCTF-2020_Rap God
## Description
My rapper friend Big Y sent me his [latest track](https://static.tjctf.org/302ed01b56ae5988e8b8ad8d9bba402a2934c71508593f5dc9e95aed913d20cf_BigYAudio.mp3) but something sounded a little off about it. Help me find out if he was trying to tell me something with it. Submit your answer as tjctf{message}

## Solution
1.  Untuk menyelesaikan _problem_ ini, kita akan menggunakan aplikasi [Sonic Visualiser](https://www.sonicvisualiser.org/) agar kita bisa mendaptkan __Waveform__ dan __Spectogram__ dari  [latest track](https://static.tjctf.org/302ed01b56ae5988e8b8ad8d9bba402a2934c71508593f5dc9e95aed913d20cf_BigYAudio.mp3).<br>
__Waveform__ dan __Spectogram__ yang berhasil didapatkan yakni:<br>
![01](https://user-images.githubusercontent.com/49342639/83140970-1b26bf80-a119-11ea-92bf-dce8fb295fd7.jpg)
	<br>Dapat kita lihat bahwa terlihat pada gambar di atas ternyata terdapat __Winding Characters__. Oleh karena itu, kita akan mendapatkan ```flag``` dengan mendeskripsikan makna dari karakter tersebut dan berikut merupakan __Tabel Winding Characters__: <br>
	![02](https://user-images.githubusercontent.com/49342639/83141464-ef580980-a119-11ea-9f6c-c4785c4d6dd9.jpg)


## Flag
```html
tjctf{QUICKSONIC}
```
Hidden characters, but unhidden point :unlock:<br>
![Solve17](https://user-images.githubusercontent.com/49342639/83141721-5d9ccc00-a11a-11ea-9bcc-db048064fa39.PNG)
