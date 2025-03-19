# Lab 7 & 8

---

## Experiment Description
This lab focuses on managing directories, setting permissions using symbolic and octal methods, and configuring the `umask` for a user. The tasks include creating directories, modifying permissions, and ensuring proper access control.

---

## Approach

### 1. Creating the `/home/consultants` Directory
The `mkdir` command is used to create the directory.

#### Command:
```bash
sudo mkdir /home/consultants
```

#### Screenshot:
![Screenshot from 2025-03-19 14-47-48](https://github.com/user-attachments/assets/77284eeb-4c2d-4b6a-bf7e-62f109a04355)


---

### 2. Adding Write Permission to the `consultants` Group
The `chmod` command with the symbolic method is used to grant write permissions to the group.

#### Command:
```bash
sudo chmod g+w /home/consultants
```

#### Explanation:
- `g+w`: Adds write (`w`) permission for the group (`g`).

#### Screenshot:
![Screenshot from 2025-03-19 14-49-49](https://github.com/user-attachments/assets/d3db32b3-1751-44f8-b2fa-aa2930d1a38c)


---

### 3. Restricting Access for Others
The `chmod` command with the octal method is used to restrict access for others.

#### Command:
```bash
sudo chmod 770 /home/consultants
```

#### Explanation:
- `770`: 
  - `7` (owner): Full permissions (read, write, execute).
  - `7` (group): Full permissions (read, write, execute).
  - `0` (others): No permissions.

#### Screenshot:
![Screenshot from 2025-03-19 14-50-29](https://github.com/user-attachments/assets/ab0bd1a3-82b5-4451-b216-955c79b14c33)


---

### 4. Verifying Directory Permissions
The `ls -ld` command is used to check the permissions of the directory.

#### Command:
```bash
ls -ld /home/consultants
```

#### Expected Output:
```
drwxrwx--- 2 root consultants 4096 Oct 10 12:34 /home/consultants
```

#### Screenshot:
![Screenshot from 2025-03-19 14-51-21](https://github.com/user-attachments/assets/4aa01fb0-8fcb-41bc-a274-050ba227c123)


---

### 5. Modifying the Default `umask` for a User
The `umask` determines the default permissions for newly created files and directories.

#### Steps:
1. Switch to the `operator1` user:
   ```bash
   sudo su - operator1
   ```
2. Update the `umask` value in the user's shell configuration file:
   ```bash
   echo "umask 007" >> ~/.bashrc
   ```
3. Apply the changes:
   ```bash
   source ~/.bashrc
   ```
4. Verify the updated `umask`:
   ```bash
   umask
   ```

#### Explanation:
- `umask 007`: 
  - `0` (owner): Full permissions.
  - `0` (group): Full permissions.
  - `7` (others): No permissions.

#### Screenshot:

![Screenshot from 2025-03-19 15-01-57](https://github.com/user-attachments/assets/e4ba1980-4fd1-4eda-b546-d3c4336da381)

![Screenshot from 2025-03-19 15-01-26](https://github.com/user-attachments/assets/7fe2de39-c108-4687-9f7a-4501e2b81359)

![Screenshot from 2025-03-19 15-08-15](https://github.com/user-attachments/assets/778bfcf3-3e69-469d-bd6c-0f486b72214c)




## Conclusion
In this lab, you practiced:
1. Creating directories and managing their permissions using symbolic and octal methods.
2. Restricting access to specific users and groups.
3. Configuring the `umask` to control default permissions for files and directories.
