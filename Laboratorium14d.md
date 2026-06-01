Sprawozdanie - Lab 14d

Zmiany:
Usunąłem jawne hasła z pliku docker-compose.yml. Zamiast tego stworzyłem pliki db_root_password.txt i db_password.txt, do których wpisałem hasła. W pliku yml na samym dole dodałem sekcję secrets, a w ustawieniach MySQL zmieniłem zmienne na MYSQL_ROOT_PASSWORD_FILE i MYSQL_PASSWORD_FILE. Dzięki temu Docker sam zaczytuje hasła prosto z plików.

Użyte komendy:
docker compose up -d (odpalenie w tle)
docker compose ps (sprawdzenie kontenerów)
docker compose down (wyłączenie i usunięcie)

Dowody działania:
Wszystko działa tak samo jak przed zmianami.
Nginx i PHP: pod adresem localhost:4001 ładuje się strona index.php.
MySQL i phpMyAdmin: logowanie na localhost:6001 działa poprawnie. Użyłem hasła z pliku tekstowego i bez problemu wszedłem na konto root.

![ps-secrets](ps-secrets.png)
![php-po-zmianie](php-po-zmianie.png)
![logowanie-po-zmianach](logowanie-po-zmianach.png)