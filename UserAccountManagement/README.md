# 🔐 User Account Management Bash Script
This Bash script provides a simple command-line interface to manage user accounts on a Linux system. It supports creating, deleting, listing, and resetting passwords for user accounts.

## 📄 Features

- Create a new user account  
- Delete an existing user account  
- Reset the password of an existing user  
- List all system user accounts  
- Display help information  

## 🧰 Requirements

- Linux environment (Tested on Debian/Ubuntu-based systems)  
- Root or sudo privileges (most operations like `useradd`, `userdel`, and `chpasswd` require elevated permissions)

## 📦 Usage

```bash
./user_manager.sh [OPTIONS]
````

### ✅ Options

| Option           | Description                          |
| ---------------- | ------------------------------------ |
| `-c`, `--create` | Create a new user account            |
| `-d`, `--delete` | Delete an existing user account      |
| `-r`, `--reset`  | Reset password for an existing user  |
| `-l`, `--list`   | List all user accounts on the system |
| `-h`, `--help`   | Display help/usage information       |

## 🔐 Permissions

To make the script executable:
```bash
chmod +x user_manager.sh
```

Run it with:
```bash
sudo ./user_manager.sh -c
```