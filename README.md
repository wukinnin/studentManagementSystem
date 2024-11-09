# 0 -- initial setup

Start fresh laravel project
```
composer create-project laravel/laravel studentManagementSystem --ignore-platform-req=ext-fileinfo
```

Initialize git
```
git init
git add .
git commit -m "[message]"
```

add git repo to github
```
git remote add origin [link.git]
git branch -M main
git push -u origin main
```



---

# 0.5 -- if starting from a clone 
*(2 is variable)*

0.
```
php.ini
# uncomment ;extension=fileinfo
# to extension=fileinfo
```

1.
```
cp .env.example .env
php artisan key:generate
```

2.
```
composer install
composer require laravel/breeze --dev
php artisan breeze:install
php artisan migrate
npm install
npm build install
```

3. .env file
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

4.
```
php artisan migrate
```

---
