# LEMP Stack with Docker Compose for WordPress 🚀

![LEMP Stack](https://img.shields.io/badge/LEMP%20Stack-Docker%20Compose-blue?style=flat&logo=docker)

Welcome to the **LEMP-stack-docker-compose** repository! This project provides a streamlined way to set up a WordPress site using a complete LEMP stack (Linux, Nginx, MySQL, PHP) inside Docker containers. The setup process is automated through a bash script, making it easy for developers and enthusiasts to get started quickly.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Bash Script Functions](#bash-script-functions)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Introduction

This project simplifies the deployment of a WordPress site by leveraging the power of Docker and Docker Compose. With just a few commands, you can have a fully functional LEMP stack ready for development or production. The bash script included in this repository automates the entire setup process, ensuring you have the latest version of WordPress and all necessary configurations.

## Features

- **Automated Setup**: A bash script that checks dependencies, pulls the latest WordPress version, and manages the site lifecycle.
- **Containerization**: Each component runs in its own Docker container, providing isolation and ease of management.
- **LEMP Stack**: Combines Linux, Nginx, MySQL, and PHP for a powerful web hosting environment.
- **Easy Management**: Start, stop, or delete your site with simple commands.
- **Local Development**: Ideal for local development and testing before deployment.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)
- Basic knowledge of command-line operations

## Installation

To get started with this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/nervisking/LEMP-stack-docker-compose.git
   cd LEMP-stack-docker-compose
   ```

2. Download the bash script and execute it:
   You can find the script in the [Releases section](https://github.com/nervisking/LEMP-stack-docker-compose/releases). Download the latest release, and then run:
   ```bash
   bash setup.sh
   ```

3. Follow the prompts in the script to complete the setup.

## Usage

Once the setup is complete, you can manage your WordPress site using the following commands:

- **Start the site**:
  ```bash
  docker-compose up -d
  ```

- **Stop the site**:
  ```bash
  docker-compose down
  ```

- **Delete the site**:
  ```bash
  bash setup.sh delete
  ```

You can also access your WordPress site by navigating to `http://localhost` in your web browser.

## Project Structure

The project is organized as follows:

```
LEMP-stack-docker-compose/
│
├── docker-compose.yml
├── nginx/
│   └── default.conf
├── php/
│   └── Dockerfile
├── mysql/
│   └── init.sql
└── setup.sh
```

- **docker-compose.yml**: The main configuration file for Docker Compose.
- **nginx/**: Contains Nginx configuration files.
- **php/**: Contains the Dockerfile for the PHP container.
- **mysql/**: Contains SQL scripts for initializing the MySQL database.
- **setup.sh**: The bash script that automates the setup process.

## Bash Script Functions

The `setup.sh` script includes several key functions to facilitate the setup and management of your WordPress site:

1. **Check Dependencies**: Verifies that Docker and Docker Compose are installed.
2. **Pull Latest WordPress**: Downloads the latest version of WordPress.
3. **Generate /etc/hosts Entries**: Adds entries to your hosts file for local access.
4. **Manage Site Lifecycle**: Functions to start, stop, and delete the site.

## Troubleshooting

If you encounter issues during the setup or usage, consider the following:

- Ensure Docker and Docker Compose are installed correctly.
- Check the Docker logs for any error messages:
  ```bash
  docker-compose logs
  ```
- Make sure no other services are running on the same ports.

## Contributing

We welcome contributions to improve this project. If you have suggestions or find bugs, please create an issue or submit a pull request.

1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Commit your changes and push to your fork.
4. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Links

For more information, visit the [Releases section](https://github.com/nervisking/LEMP-stack-docker-compose/releases) to download the latest setup script and execute it for your project.

Explore the power of Docker and the LEMP stack with this easy-to-use setup for WordPress. Enjoy developing your site!