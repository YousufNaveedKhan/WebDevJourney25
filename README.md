# WebDevJourney25: SQL, PHP and Laravel

Course material for a **web backend development** course taught by **Yousuf Naveed Khan**, Senior Instructor at Aptech Gulshan-2, Karachi, to Batch AI-2025-01B (November 2025 to January 2026).

The course takes a student from database design in **MySQL**, through **Core PHP** (including a login system and a mini blog), to modern backend development with **Laravel 12**. It focuses on server-side development and databases, so the front end is kept simple (Bootstrap, and a little jQuery for AJAX).

Each lecture folder holds the code that was built in class. The course grows from simple to advanced, so the earlier lectures are basic on purpose.

## Tech stack

| Area | What is used |
|---|---|
| **Database** | MySQL, with phpMyAdmin or MySQL Workbench |
| **SQL topics** | DDL and DML, aggregate functions, relationships and keys, joins, views, subqueries, stored procedures, triggers, transactions, indexes, user privileges, backup and recovery |
| **Core PHP** | PHP 8 (procedural and object-oriented), `mysqli`, sessions, cookies, file handling, file uploads, `password_hash` |
| **Framework** | Laravel 12 (PHP 8.2 or newer), Blade, Eloquent ORM, migrations, routing, controllers, Artisan |
| **API work** | JSON endpoints in PHP, AJAX with jQuery 3.7, consuming an external REST API from Laravel (Quran API) |
| **UI** | Bootstrap 5.3 |
| **Tools** | XAMPP (Apache and MySQL), Composer, SQLite (Laravel's default development database), Git |

## What is inside

| Module | Content | What you learn |
|---|---|---|
| [`01_MySQL`](./01_MySQL) | 13 lectures | SQL from first table to backup and security |
| [`02_PHP`](./02_PHP) | 14 lectures, 2 projects, 2 assignments | Core PHP, CRUD, authentication, OOP and AJAX |
| [`03_Laravel`](./03_Laravel) | 6 lecture projects | Laravel 12, Blade, API integration and Eloquent CRUD |

## 01_MySQL

Each lecture is one `.sql` script. Run it in phpMyAdmin or MySQL Workbench and follow along.

| Lecture | Topic |
|---|---|
| 01 | Database and table creation, inserting data |
| 02 | Database operations and data manipulation (CRUD) |
| 03 | Aggregate functions and table alteration |
| 04 | Relationships and keys |
| 05 | Joins and views |
| 06 | Subqueries and nested queries |
| 07 | Stored procedures and functions |
| 08 | Triggers and transactions |
| 09 | Indexes and performance optimization |
| 10 | Data security and user management |
| 11 | Advanced query techniques |
| 12 | Database backup and recovery |
| 13 | NoSQL integration and hybrid systems (notes) |

## 02_PHP

| Lecture | Topic |
|---|---|
| 01 | Basics |
| 02 | Loops |
| 03 | Arrays |
| 04 | Array methods |
| 05 | String manipulation |
| 06 | Form handling |
| 07 | GET method and sessions |
| 08 | Cookies |
| 09 | File handling |
| 10 | Path handling |
| 11 | CRUD with MySQL |
| 12 | File uploading |
| 13 | Object-oriented PHP (a small login system with models and controllers) |
| 14 | API and AJAX |

### Projects

* **Login and Registration System** (`Projects/LRS`): register, log in and log out, passwords stored as hashes, sessions, and separate pages for the `admin` and `user` roles.
* **Mini Blog App** (`Projects/MiniBlog App`): register and log in, create, edit and delete posts, and upload profile pictures, with a Bootstrap interface.

### Assignments

* **Mini Blog Application**: students build the blog on their own, with authentication, authorization, CRUD and secure coding.
* **CV Uploader and Image Uploader**: file upload with validation, database storage, listing and deleting records.

The assignment briefs are in [`02_PHP/Assignments`](./02_PHP/Assignments). Submissions are by GitHub only.

## 03_Laravel

Every folder is a complete Laravel 12 project.

| Folder | Topic |
|---|---|
| `lec01-introduction` | Installing Laravel and understanding the project structure |
| `lec02-routingandbladetemplatingengine` | Routes, views and Blade templates |
| `lec03-quranAPI` | A controller that consumes the Al Quran Cloud API: list the surahs and read a surah |
| `lec04-repeat-fatima` | Revision of the Quran API project |
| `lec05-eloquentModel-1` | Eloquent model, migration and listing posts |
| `lec06-eloquentModel-CRUD` | Full CRUD with Eloquent: add, edit and delete posts |

## Getting started

You need: **XAMPP** (Apache and MySQL), **PHP 8.2 or newer** and **Composer** (for Laravel), and **Git**.

### MySQL

1. Start MySQL in the XAMPP Control Panel and open phpMyAdmin.
2. Open a lecture's `.sql` file, then run it (Import, or paste it in the SQL tab).

### PHP

1. Copy the `02_PHP` folder into `C:\xampp\htdocs\`.
2. Start **Apache** and **MySQL** in the XAMPP Control Panel.
3. Create the database a lecture needs. The names used in the code are:

   | Code | Database name |
   |---|---|
   | `Lec11-CRUD` | `lec11-crud` |
   | `Lec13-OOP` | `students` |
   | `Projects/LRS` | `lrs` |
   | `Projects/MiniBlog App` | `miniBlog` |

4. Open `http://localhost/02_PHP/` and choose a lecture.

The projects connect as `root` with an empty password, which is the XAMPP default for **local learning only**. Never use these settings on a real server.

### Laravel

```bash
git clone https://github.com/YousufNaveedKhan/WebDevJourney25.git
cd WebDevJourney25/03_Laravel/lec06-eloquentModel-CRUD
composer install
copy .env.example .env        # on macOS or Linux: cp .env.example .env
php artisan key:generate
php artisan migrate           # answer "yes" if it offers to create the SQLite database
php artisan serve
```

Open `http://127.0.0.1:8000`. Use the same steps for any other lecture folder. The Quran API lectures (`lec03` and `lec04`) need an internet connection.

## About the instructor

**Yousuf Naveed Khan** is a software architect, educator and Hafiz-e-Quran based in Karachi, Pakistan, Founder & CEO of [GFT Solutions](https://wearegft.com) and Senior Instructor at Aptech Gulshan-2.

[Website](https://yousufnaveedkhan.com) · [LinkedIn](https://www.linkedin.com/in/yousufnaveedkhan/) · [More course repositories](https://github.com/YousufNaveedKhan?tab=repositories)
