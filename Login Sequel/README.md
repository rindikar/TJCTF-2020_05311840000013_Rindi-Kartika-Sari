# TJCTF-2020_Login Sequel
## Description
[Login](http://login_sequel.tjctf.org/) as admin you must. This time, the client is of no use :(. What to do? <br>
![01](https://user-images.githubusercontent.com/49342639/83131225-b879f780-a109-11ea-8821-b8c9b4ffdfab.PNG)

## Solution
1. Lakukan __inspect element__ dari website tersebut dengan klik tombol __F12__ pada keyboard  dan tinjau **_Database script_** pada bagian __Source__<br>
![02](https://user-images.githubusercontent.com/49342639/83132132-24109480-a10b-11ea-88b2-55c7bb290289.PNG)

	```html
	def get_user(username, password):
	    database = connect_database()
	    cursor = database.cursor()
	    try:
	        cursor.execute('SELECT username, password FROM `userandpassword` WHERE username=\'%s\' AND password=\'%s\'' % (username, hashlib.md5(password.encode())))
	    except:
	        return render_template("failure.html")
	    row = cursor.fetchone()
	    database.commit()
	    database.close()
	    if row is None: return None
	    return (row[0],row[1])
	```
2. Penyelesaian termudah adalah melakukan **_login_** dengan menggunakan __username__ : ```admin' /*``` dan __password__```bebas```<br>
![03](https://user-images.githubusercontent.com/49342639/83132889-40f99780-a10c-11ea-99c6-ffbccd2ac42c.PNG)
	<br> Form telah diisi dan mari kita lihat hasilnya dengan klik **_Login button_**<br>
	![04](https://user-images.githubusercontent.com/49342639/83133047-7605ea00-a10c-11ea-9c3f-a2537c68f085.PNG)

## Flag
```html
tjctf{W0w_wHa1_a_SqL1_exPeRt!}
```
wow, we got it right :gem: <br>
![Solve16](https://user-images.githubusercontent.com/49342639/83133309-e4e34300-a10c-11ea-83f3-fedfa785e51b.PNG)
