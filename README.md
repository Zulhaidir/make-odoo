
#### Running Odoo Application menggunakan "-- --dev all"
1. Dengan adanya "command: -- --dev all" pada docker-compose.yaml
```sh
command: -- --dev all
```
2. Ketika update file python ataupun xml, kita tidak perlu me-restart docker CLI atau desktop (GUI)
3. Ketika update file xml, kita hanya me-refresh browser
4. Ketika update file python, kita melakukan upgrade module dan sekaligus me-refresh browser

#### Running Odoo Application menggunakan "odoo -u nama_module -d nama_database"
1. Dengan adanya "command: odoo -u nama_module -d nama_database" pada docker-compose.yaml
```sh
command: odoo -u nama_module -d nama_database
```
2. Ketika update file python ataupun xml, kita harus me-restart di docker CLI atau desktop (GUI)
3. Ketika update file xml, restart docker CLI atau desktop (GUI), lalu me-refresh browser
4. Ketika update file python, restart docker CLI atau desktop (GUI), lalu me-refresh browser, tidak perlu upgrade module secara manual, module terupgrade setelah di docker CLI atau GUI direstart

#### Membuat Module Baru dengan cepat
```sh
docker-compose exec web /usr/bin/odoo scaffold nama_module /mnt/extra-addons && sudo chmod -R 777 custom-addons/nama_module
```
1. /usr/bin/odoo, bisa dilihat pada exec odoo pada docker desktop, lalu ketik which odoo, maka akan muncul dimana odoo berada
2. nama_module, buat nama module yang anda inginkan
3. /mnt/extra-addons, bisa dilihat pada file docker-compose.yaml, terdapat pada volume
4. sudo chmod -R 777, kita melakukan chmod agar kita dapat mengedit module yang dibuat
5. custom-addons/nama_module, yaitu pada directory custom_addons dan didalamnya module yang dibuat

