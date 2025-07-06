# User-Management

This project provides a simple bash script to automate user creation on Linux systems.

## 📜 Script Overview

The script `user_make.sh` performs the following tasks:

- Ensures the script is run with `sudo` or root privileges
- Accepts a username (required) and an optional comment (e.g., full name or role)
- Automatically generates a secure password
- Creates the user with the specified details
- Sets the generated password
- Forces the user to change the password on first login
- Outputs the username, password, and hostname for reference

## 🚀 Usage

```bash
sudo ./user_make.sh USER_NAME [COMMENT...]
````

* `USER_NAME`: The login name of the new user (required)
* `COMMENT`: Optional comment, such as full name or role

### Example:

```bash
sudo ./user_make.sh johndoe "John Doe - Developer"
```

## 🛡️ Output

After successful execution, the script displays:

* Username
* Generated password
* Hostname of the machine

## ⚠️ Notes

* This script must be executed with `sudo` or as root.
* Password is generated based on the current timestamp (`date +%s%N`) and is meant to be temporary.
* The user will be prompted to set a new password on first login.

## 📁 Files

* `user_make.sh`: The main script to create users

## 🧑‍💻 Author

* GitHub: [BitGladiator](https://github.com/BitGladiator)
