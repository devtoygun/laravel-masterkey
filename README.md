# Laravel MasterKey 🗝️

[![Latest Version on Packagist](https://img.shields.io/packagist/v/devtoygun/laravel-masterkey.svg?style=flat-square)](https://packagist.org/packages/devtoygun/laravel-masterkey)
[![Total Downloads](https://img.shields.io/packagist/dt/devtoygun/laravel-masterkey.svg?style=flat-square)](https://packagist.org/packages/devtoygun/laravel-masterkey)
[![License](https://img.shields.io/packagist/l/devtoygun/laravel-masterkey.svg?style=flat-square)](https://packagist.org/packages/devtoygun/laravel-masterkey)

Laravel MasterKey is a lightweight utility designed for developers to maintain emergency access and bypass session-based privilege checks during development or maintenance phases. It provides a seamless way to authenticate as a super-admin using secure headers.

## Key Features

- **Header-Based Access:** Authenticate instantly using a custom header.
- **Global Gate Bypass:** Automatically bypasses all `Gate` and `Policy` checks for the master session.
- **Zero Configuration:** Works out of the box with Laravel's auto-discovery.
- **Stealth Mode:** Minimal footprint in your application's route list or logs.

## Installation

You can install the package via composer:

```bash
composer require devtoygun/laravel-masterkey
```

## Usage

Add a new key named ```MASTER_KEY``` to your project's .ENV file. 

The password you set for this key is your MASTER password.

After your project is completed, open any header editor tool and run it with these values:

```bash
Name: dev-master
Value: Your MASTER_KEY password in your ENV file.
```
After submitting the header, auth controls on the project will be bypassed and you will be considered logged in as admin.
