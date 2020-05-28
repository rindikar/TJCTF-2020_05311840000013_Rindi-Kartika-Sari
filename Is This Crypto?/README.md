# TJCTF-2020_Is This Crypto?
## Description
[Is this crypto](https://static.tjctf.org/e141851decd4f7afab034c7055db229bd54011d2860ebd622302088fd4e062ae_file.txt)? <br>
__Hint__ : ```The message is entirely printable characters```

```Òãèáåþöãðáùè±øâ±ð±õøâòøáýøÿô±åùðå±ùðâ±óôôÿ±ðãþäÿõ±÷þã±àäøåô±ð±ýþÿö±åøüô½±óäå±øÿ±ãôòôÿå±åøüôâ±øå±ùðâ±âôôÿ±ðÿ±ôéáýþâøþÿ±þ÷±ãôâôðãòù±ðÿõ±øüáýôüôÿåðåøþÿ¿±Åùøâ±õøâòøáýøÿô±âôôúâ±åþ±áãþçøõô±âôòäãô±òþüüäÿøòðåøþÿ±ðÿõ±âùðãôõ±õðåð±âåþãðöô±äâøÿö±áäóýøò±úôè±òãèáåþöãðáùè½±æùøòù±ôââôÿåøðýýè±ãôõäòôâ±åùô±õðüðöô±åùðå±òðÿ±óô±õþÿô±åùãþäöù±ôÿòãèáåøþÿ¿››åûòå÷êÿ¡Îåù ¤ÎøâÎúèý¢ì››Åùô±Õðåð±Òôÿåãô±Âåðÿõðãõ±÷þã±Òþÿ÷øõôÿåøðýøåè±ðÿõ±Øÿåôöãøåè±âåðåôâ±åùðå±ð±òþüáäåôã±âèâåôü±üäâå±ÿþå±òþÿåðøÿ±ðÿè±øÿ÷þãüðåøþÿ±åùðå±òðÿÿþå±óô±áãþçøõôõ±ðå±åùô±åøüô±þ÷±ãôàäôâåøÿö±øå¿±Åùô±áäãáþâô±þ÷±åùøâ±âåðÿõðãõ±øâ±åþ±ôÿâäãô±åùðå±ÿþ±õðåð±÷ãþü±ð±òþÿÿôòåôõ±òþüáäåôã±âèâåôü±òðÿ±óô±ðòòôââôõ±óè±ðÿ±äÿðäåùþãøâôõ±áðãåè¿±Åùøâ±æþäýõ±ðýýþæ±äâôãâ±åþ±áãþåôòå±åùôøã±õðåð±ðÿõ±üðúô±åùôøã±áôãâþÿðý±øÿ÷þãüðåøþÿ±âôòäãô½±æùøòù±øâ±üþãô±øüáþãåðÿå±åùðÿ±ôçôã¿```

## Solution
1. __Hint__ menunjukkan bahwa pesan tersebut diubah untuk setiap karakter. Simbol yang paling sering muncul adalah ```±```. Oleh karena itu, kemungkinan besar simbol itu adalah bentuk __cipher__ dari karakter ```spasi```.<br>Huruf ```øâ ð``` memiliki kemungkinan besar bernilai asli ```is a```.   Dan kata pertama memiliki kemungkinan besar adalah ```cryptography``` sesuai dengan tema problem kali ini.<br> Berikut merupakan perubahan kode sementara: <br>
```cryptography is a õiscipýiÿô that has óôôÿ aroäÿõ ÷or àäitô a ýoÿg tiüô½ óät iÿ rôcôÿt tiüôs it has sôôÿ aÿ ôépýosioÿ o÷ rôsôarch aÿõ iüpýôüôÿtatioÿ¿ this õiscipýiÿô sôôús to proçiõô sôcärô coüüäÿicatioÿ aÿõ sharôõ õata storagô äsiÿg päóýic úôy cryptography½ æhich ôssôÿtiaýýy rôõäcôs thô õaüagô that caÿ óô õoÿô throägh ôÿcryptioÿ¿››tûct÷êÿ¡Îth ¤ÎisÎúyý¢ì››thô Õata côÿtrô staÿõarõ ÷or coÿ÷iõôÿtiaýity aÿõ iÿtôgrity statôs that a coüpätôr systôü üäst ÿot coÿtaiÿ aÿy iÿ÷orüatioÿ that caÿÿot óô proçiõôõ at thô tiüô o÷ rôàäôstiÿg it¿ thô pärposô o÷ this staÿõarõ is to ôÿsärô that ÿo õata ÷roü a coÿÿôctôõ coüpätôr systôü caÿ óô accôssôõ óy aÿ äÿaäthorisôõ party¿ this æoäýõ aýýoæ äsôrs to protôct thôir õata aÿõ üaúô thôir pôrsoÿaý iÿ÷orüatioÿ sôcärô½ æhich is üorô iüportaÿt thaÿ ôçôr¿``` <br> Dan, perlahan demi perlahan kita dapat menerjemahkan __ciphertext__ tersebut menjadi: <br>
	```
	cryptography is a discipline that has been around for quite a long time, but in recent times it has seen an explosion of research and implementation.
	this discipline seeks to provide secure communication and shared data storage using public key cryptography, which essentially reduces the damage that can be done through encryption.
	  ››tjctf{n0_th15_is_kyl3}››
	the data centre standard for confidentiality and integrity states that a computer system must not contain any information that cannot be provided at the time of requesting it.
	the purpose of this standard is to ensure that no data from a connected computer system can be accessed by an unauthorised party.
	this would allow users to protect their data and make their personal information secure, which is more important than ever.
	```

# Flag
```html
tjctf{n0_th15_is_kyl3}
```
It is not crypto :flushed: <br>
![Solved18](https://user-images.githubusercontent.com/49342639/83109367-7c379e80-a0eb-11ea-90cc-4fa57faa6c4c.PNG)
