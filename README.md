#### Running Odoo Application menggunakan "-- --dev all"
1. Dengan adanya "command: -- --dev all" pada docker-compose.yaml
2. Ketika update file python ataupun xml, kita tidak perlu me-restart docker CLI atau desktop (GUI)
3. Ketika update file xml, kita hanya me-refresh browser
4. Ketika update file python, kita melakukan upgrade module dan sekaligus me-refresh browser

#### Running Odoo Application menggunakan "odoo -u nama_module -d nama_database"
1. Dengan adanya "command: odoo -u nama_module -d nama_database" pada docker-compose.yaml
2. Ketika update file python dan xml, kita harus me-restart di docker CLI atau desktop (GUI)
3. Ketika update file xml, restart docker CLI atau desktop (GUI), lalu restart browser
4. Ketika update file python, restart docker CLI atau desktop (GUI), lalu restart browser, tidak perlu upgrade module secara manual, module terupgrade setelah di docker CLI atau GUI direstart
