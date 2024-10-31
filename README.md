# mysql-phpmyadmin-docker
A MySQL development environment with Docker and phpMyAdmin for learning MySQL 

# Setting Up a Codespace in GitHub (Cloud-Based Development Environment)

Follow the steps below to set up a GitHub Codespace. Codespaces offer a cloud-based development environment that makes it easy to get started without any local setup.

### Step 1: Clone the Repository
1. **Clone this repository** to your own GitHub account by clicking the "Fork" button in the top right corner of the repository page.

### Step 2: Set Up a Codespace Secret
1. Navigate to **your repository** on GitHub.
2. Click on the **Settings** tab at the top of the repository page.
3. In the left sidebar, scroll down and find the **"Secrets and variables"** section.
4. Click on **Codespaces** under this section.
5. Click the **New repository secret** button.
6. Provide a unique name for the secret, using **UPPERCASE letters with underscores** (Use **MYSQL_PASSWORD** as the variable name, as it is defined with the same name in docker-compose.yml).
7. **Enter the secret value** in the text box (e.g., your database password). This will be your password for logging in to the database within the Codespace environment.
8. Click the **"Add secret"** button to save the secret.

### Step 3: Create a Codespace
1. Go back to your repository's **main page**.
2. Click the **"Code"** button (usually located near the top right).
3. Select **"Create codespace on main"**.
4. Wait for a few moments while your Codespace environment is being set up.
---

## Using phpMyAdmin in GitHub codespace

### Step 5: Open Port 6033
1. Open the **Ports** view in your Codespace.
2. Click on **"Add Port"**.
3. Enter **6033** as the port number to expose.
4. Once port 6033 is successfully added, it will appear in the Ports view.

### Step 6: Open Port 88 for phpMyAdmin
1. Open the **Ports** view in your codespace.
2. Click **Add Port** and enter **88** as the port number.
3. Once the port is added, a forwarded address for port 88 will appear. Click on the forwarded address to open phpMyAdmin.
5. Use your MySQL credentials to log in and start working with your databases.

![Example Ports](https://raw.githubusercontent.com/dipaish/dipaish/refs/heads/main/images/courseRelatedImages/ports.png)

> **Note**: It is important to verify that both **ports 88 and 6033 are open and forwarded** correctly to avoid any connectivity issues while working with your databases.

> **Note**: If you delete your current Codespace and create a new one, **all databases and tables you’ve created will be lost**. To preserve them, make sure to back up your data using the database import/export functions.

---

## Connecting to MySQL Database in codespace with CLI

After the codespace starts, you can log in to the MySQL database server using the following command:

```bash
mysql -u <username> -p
```

> Replace <username> with your MySQL username. Enter your password when prompted. Once logged in, you can execute SQL queries, such as creating databases, tables, and more.

![Example connection](https://raw.githubusercontent.com/dipaish/dipaish/refs/heads/main/images/courseRelatedImages/dataBase.png)

---

# Local Development Environment in your personal devices 

In addition to the Codespace environment in GitHub, you will also set up a similar development environment locally on your personal device. Please follow the guidelines below:

### Step 1: Clone the Repository 
1. **Clone the repository** to your personal device:
   ```sh
   git clone https://github.com/your-username/your-repository.git
   ``` 
### Step 2: Create a .env File
1. In the root directory of your cloned repository, create a new file named **.env** 
2. Open the .env file and add the following line and save the file
   ```sh
   MYSQL_PASSWORD=yourpassword
    ``` 
> **Note**  Replace **yourpassword** with your own password. This will be your login password for the database service in the local environment.

### Step 3: Reopen in Container (VS Code)

1. Make sure you have the **Remote - Explorer** extension installed in your local Visual Studio Code.
2. When prompted, click **Reopen in Container.**
3. Wait a couple of minutes for your local development container to set up.

> Your local environment will now be ready to use, with all required dependencies and tools installed within the container.

## Connecting to MySQL Database in the Local Environment

To connect to the MySQL database server in your local environment, you will use **MySQL Workbench**. Follow the steps below to set up the connection.

### Step 1: Start MySQL Workbench
1. **Open MySQL Workbench** on your computer.
2. Click the **"+" (Add Connection)** button to create a new connection.

### Step 2: Configure the Connection
1. **Provide a Connection Name**: Enter a name that you will recognize later (e.g., "Local MySQL Connection").
2. **Hostname**: Set the hostname to `127.0.0.1`.
3. **Port**: Enter `6033` as the port number.
4. **Username**: Set the username to `root`.

### Step 3: Test the Connection
1. Click on **"Test Connection"** to verify the connection settings.
2. When prompted, enter the **password**: Use the password you specified in your `.env` file (`MYSQL_PASSWORD`).
3. If the connection is successful, you will see a confirmation message.

### Step 4: Save the Connection
1. Click **"OK"** to save the connection.
2. Optionally, check **"Store in Vault"** to save your password for future use, so you don’t need to re-enter it each time.

### Step 5: Connect to the Database
- The new connection will now appear in the **Welcome** section of MySQL Workbench.
- To connect in the future, simply click on the **connection name** and it will connect you to the database server automatically.

> **Tip**: Storing the password in the vault will make connecting to your database faster and more convenient.