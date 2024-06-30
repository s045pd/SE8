# 🎨 Unorthodox Comic Project
> By GPT-4o+Claude

Welcome to the wacky world of our Unorthodox Comic Project! This guide will help you navigate through the whimsical chaos.

## 📖 Overview

This project is a playful, irreverent comic generator that promises to bring a smile (or a groan) to your face. Dive in and explore the hilarity!


## 🛠️ Installation

First, ensure you have Python installed on your system. Then, clone the repository and navigate to the project directory:

```bash
git clone <repository-url>
cd <project-directory>
```

Install the necessary dependencies with pip:

```bash
pip install -r requirements.txt
```


## ⚙️ Configuration

Adjust the settings in SE8/settings.py to suit your preferences. Key configurations include:

> Database: Ensure your database settings are correctly configured.
> Middleware: Check and modify any middleware components if needed.


## 🚀 Running the Project
To run the project locally, use the following command:

```bash
python manage.py runserver
```

Access the project in your browser at http://127.0.0.1:8000/.

## 🖥️ Usage

This project is automated, minimizing manual input. Here are the main actions:

1. Start Finding Books

	- Use the <span style="color:red"><strong>"Start Find Books"</strong> </span> button at the top to initiate the book-finding process.

2. Books Management

	- View the list of books under the "Books" section in the navigation panel.
	- Actions: Use the dropdown menu to select actions for managing books, such as updating or deleting entries.
	- Read: Click the "Read" button next to a book title to view its episodes.

3. Apps Management

	- Navigate through the various sections like Books, Episodes, Images, and Tags under the "APPS" menu.
	
	- Each section allows you to perform specific actions related to the management of comics content.

4. Filter and Search

	- Use the search bar to quickly find specific books or episodes.
	
	- Apply tags from the right sidebar to filter content based on different categories.

## 🛠️ Actions from admin.py

Based on the admin.py file, here are the actions you can perform:

- get_images: Fetches images for the selected books.

- convert_to_pdf: Converts the selected books to PDF format.

- convert_to_pdf_force: Forcefully converts the selected books to PDF, even if they already exist.

- refresh_images: Refreshes the images for the selected books.

## 🌀 Starting Celery

To ensure background tasks run smoothly, you need to start Celery. Use the following command to start the Celery worker:

```bash
celery -A SE8 worker --loglevel=info
```

Additionally, start the Celery beat scheduler to handle periodic tasks:

```bash
celery -A SE8 beat --loglevel=info
```

## 🐳 Using Docker
To run the project using Docker, follow these steps:

### Build and Run the Docker Image:

Use the provided docker_image_rebuild.sh script to build the Docker image and start the container:

```bash
export USE_SQLITE=True && bash docker_image_rebuild.sh
```

This script will stop any running containers, build a new Docker image, and start the new container, making the project accessible at `http://127.0.0.1:8000/`.

### Configuration:

Ensure you have configured your .env file properly. Note that using SQLite (`USE_SQLITE`) may have performance issues.

## 🐳 Using Docker-Compose


To run the project using Docker Compose, follow these steps:

1. Build and Start Services:

	Use the provided docker_compose_rebuild.sh script to build and start the Docker Compose services:

```bash
bash docker_compose_rebuild.sh
```

This script will stop any running services, build the Docker images, and start the services as defined in your docker-compose.yml file.


2.	Configuration:
	
	Ensure you have configured your .env file properly. Note that using SQLite (USE_SQLITE) may have performance issues.



## 📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

## 📛 Disclaimer
This project is for educational purposes only. If any conflicts of interest arise, please contact us to resolve or close the project.

## 🙏 Acknowledgments
Special thanks to GPT-4o+Claude for their invaluable contributions and witty insights.

We welcome any new ideas and suggestions from the community. Thank you for your support!


> Let the comic adventures begin! 🎉