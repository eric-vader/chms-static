# CHMS-static #
This repository stores the static files required in the CHMS project. In production, the files in this repository will be hosted in a CDN. In this guide, we will show you how to setup a local CDN for use with the main project. The installation steps are written into a script(`setup.sh`) for your convenience.

1. Install npm: `# dnf install npm`
2. Install http-server: `# npm install -g http-server`
3. Install a certificate: `# openssl req -newkey rsa:2048 -new -nodes -x509 -days 3650 -keyout key.pem -out cert.pem`

After installation, you can start the http server in this directory with the following command. Similarly, for convenience, the starting of the server is in a script(`run.sh`).

1. Finally start the https server: `$ http-server -S -C cert.pem -p 2096`
