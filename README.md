# DevOps for Sky
This repo is for managing the web sites and web apps for Sky Unlimited, Inc.

It provisions the servers with the necessary dependencies and runs the Docker containers necessary to keep the sites/apps running smoothly. This includes running HAProxy to act as a proxy rather than a load balancer for the sites/apps.

This repo currently supports only the American Cabin Supply and American Yacht Supply sites on the staging server.

Future plans include adding support for the Sky Schedule web app and HAProxy as well as the sites running on the live server. These include the two aforementioned sites as well as American Accents. This will require Let's Encrypt, however.
