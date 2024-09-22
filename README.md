# inception
🖥️ Overview of the Project

The project, in which I had to deploy a small infrastructure on a Virtual Machine with the help of Docker Compose. Here’s a detail of what I did:

Structured Directory: All of my configuration files were kept in a designated srcs sub-folder as well as a Makefile kept at the root level to handle the entire system. This opened me up to learning how to sing the code organization song! 📁

Building Custom Images: A separate Docker image was needed for every service and I wrote Dockerfiles for each of them. How thrilling it was to build images of the code I wrote rather than using people’s images on the registry! 💻

🐳 What components I Implemented

NGINX with TLS: I employed an NGINX container which was given TLS only version 1.2 or 1.3. That’s one security risk taken care of, which is good in this age.

WordPress + PHP-FPM: Setting up a containerized version of WordPress without NGINX taught me the usefulness of service dependencies.

MariaDB Initialization: I made a separate container for the MariaDB in order to ensure everything operated.
