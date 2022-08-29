<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<h3> Il task chiedeva di realizzare un sistema di messaggistica criptata end to end: basato su database NoSQL (si è deciso di usare MongoDB) e back-end in Laravel. Per la comunicazione si è deciso di usare l'API Pusher. In più si è realizzato un front-end minimale in JS usando Vue. </h3>

# Configurazione
1. Clona la repository:
```
git clone https://github.com/vinzcamp8/task_laravel_chat_realtime.git
```

2. Spostati nella directory appena creata:
```
cd task_laravel_chat_realtime
```

3. Installa le dipendenze attraverso il composer:
```
composer install
```

4. Crea un nuovo database su MongoDB. Poi rinomina il file .env.example in .env e imposta il nome del tuo database.
```
DB_CONNECTION=mongodb
DB_HOST=127.0.0.1
DB_PORT=27017
DB_DATABASE=nome_del_tuo_database
DB_USERNAME=
DB_PASSWORD=
```

5. Migra gli schema nel database:
```
php artisan migrate
```

6. Vai su: https://pusher.com/. Iscriviti e crea un canale app. Vai nella sezione App Keys. Copia i dati nel file .env 
```
PUSHER_APP_ID=app_id
PUSHER_APP_KEY=key
PUSHER_APP_SECRET=secret
PUSHER_APP_CLUSTER=cluster
```

7. Genera una app key per Laravel:
```
php artisan key:generate
``` 

8. Compila e lancia il server:
```
npm run dev
``` 
```
php artisan serve
``` 
9. Vai su http://127.0.0.1:8000 da due browser diversi, crea due User e testa la Chat.