# menjalankan docker mysql dan phpadmin dari docker desktop

mendownload image mysql

    docker pull mysql

membuat container mysql

    docker run --name mysql_db_server -e MYSQL_ROOT_PASSWORD=123 -p 3306:3306 -d mysql  atau MYSQL_ALLOW_EMPTY_PASSWORD=true


mendownload image phpmyadmin

    docker pull phpmyadmin/phpmyadmin

menjalankan container phpmyadmin dan di link ke databases mysql
    docker run --name myadmin -d --link mysql_db_server:db -p 8080:80 phpmyadmin/phpmyadmin

##penjelasan 

--name : Menentukan nama container, dalam hal ini "myadmin"
-d : Menjalankan container di mode background (detached)
--link : Menyambungkan container baru ke container MySQL yang sudah ada, dalam hal ini "mysql_db_server"
-p : Meneruskan port dari container ke host, dalam hal ini 8080 untuk port host dan 80 untuk port container.
Setelah container PhpMyAdmin berhasil dijalankan, buka browser dan masukkan URL http://localhost:8080 untuk mengakses PhpMyAdmin.

Catatan: Jika menggunakan Docker Desktop untuk Windows versi 2.2.0.0 atau lebih baru, maka URL-nya akan menjadi http://localhost:8080/index.php

localhost : Merujuk ke host lokal
8080 : Merujuk ke port yang diteruskan dari container
Anda akan diminta untuk memasukkan username dan password. Username default adalah "root" dan password defaultnya kosong. Namun, sebaiknya Anda mengubah password untuk alasan keamanan.




flask db init
flask db migrate
flask db upgrade
python -m flask run

iumcvcopcrresrun

mitgklnryakrzlhj

# Activate the virtualenv (Windows)
. myenv/Scripts/activate //ini bisa di linux dan windows

kwglyrwbchzyckfw

# atau kau bisa menampilkan data dalam bentuk json menggunakan methon berikut
# result = []
#     for user in users:
#         user_data = {}
#         user_data['id'] = user.id
#         user_data['username'] = user.username
#         user_data['email'] = user.email
#         result.append(user_data)
#     return jsonify(result)