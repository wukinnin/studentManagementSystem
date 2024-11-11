# You will need

- Laravel
- Xampp
- Composer
- NPM
- Git

---

# Initial setup and tutorial

1. Configure php.ini
```
php.ini
```
on php.ini file, uncomment `;extension=fileinfo` to `extension=fileinfo`, and restart xampp servers (apache)

2. Start fresh laravel project
```
composer create-project laravel/laravel studentManagementSystem
cd studentManagementSystem
```

3. Initialize git
```
git init
git add .
git commit -m "init"
```

add git repo to github -- assuming the repository already exists

replace [link] with a valid github repo link e.g. `https://github.com/[username]/[repoName]`

```
git remote add origin [link]
git branch -M main
git push -u origin main
```

---
# Cloned repo setup on a fresh git clone

1. install composer on vendor
```
composer install
```

2. copy to new .env file
```
cp .env.example .env
```

3. modify .env file

Change DB_DATABASE if needed.
If new, create new database with matching name in `127.0.0.1/phpmyadmin`
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=studentManagementSystem
DB_USERNAME=root
DB_PASSWORD=
```

4. generate key

```
php artisan key:generate
```

5. migrate tables
```
php artisan migrate
```

6. install breeze
   
Note: Installed livewire with dark mode support using Pest
```
composer require laravel/breeze --dev
php artisan breeze:install
php artisan migrate
```

---
