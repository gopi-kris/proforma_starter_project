# PROforma Starter Project

## Introduction

The following are instructions for setting up proformajs-vue and running a PROforma application locally.

The instructions have been tested on Ubuntu 22.04 (Linux), however, proformajs-vue will work on other operating systems (Windows, MacOS) as well.

The steps for installing dependencies will vary from one operating system to another.

A fresh installation of Ubuntu 22.04 on a [virtual machine](https://ubuntu.com/tutorials/how-to-run-ubuntu-desktop-on-a-virtual-machine-using-virtualbox#1-overview) should help to
avoid dependency issues with your local development environment.

## Software dependencies

- Git
- Node.js (version 18 is required)

## Update and upgrade Ubuntu

Run the following commands on the terminal (CTRL+ALT+T) to update and upgrade existing Ubuntu packages.

```console
foo@bar:~$ sudo apt update
foo@bar:~$ sudo apt upgrade
```

## Installing Git on Ubuntu

Run the following commands on the terminal to install Git.

```console
foo@bar:~$ sudo apt install -y git
```

Once installed you can run the following command to test the installation. You should see an output similar to the one below.

```console
foo@bar:~$ git --version
git version 2.34.1
```

## Optional

Additional instructions for configuring Git can be found here:
https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-22-04

## Installing Node.js on Ubuntu

Run the following commands on the terminal to remove existing installations of node.js, if any.

```console
foo@bar:~$ sudo apt autoremove
foo@bar:~$ sudo apt purge nodejs
```

Run the following commands on the terminal to install curl and download Node.js version 18

```console
foo@bar:~$ sudo apt install -y curl
foo@bar:~$ curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - 
```

Run the following commands on the terminal to install Node.js

```console
foo@bar:~$ sudo apt install -y nodejs
```

Once installed you can run the following commands to test the installation and versions of node.js and npm.
npm is Node Package Manager that allows the installation of packages to be used with Node.js, such as proformajs-vue.

```console
foo@bar:~$ node -v
v18.19.1
foo@bar:~$ npm -v
10.2.4
```

## Clone proformajs-vue repo

Clone the [proformajs-vue git repository](https://gitlab.com/openclinical/proformajs-vue) to the home directory of the user (or any directory) on Ubuntu and complete installation.

```console
foo@bar:~$ git clone https://gitlab.com/openclinical/proformajs-vue.git
```

## Install proformajs-vue

Change directory to the directory where proformajs-vue repository was cloned

```console
foo@bar:~$ cd proformajs-vue
```

Run the following command on the terminal to install proformajs-vue

```console
foo@bar:~$ npm install
```

Run the following command on the terminal to run proformajs-vue

```console
foo@bar:~$ npm run dev
```

If successful, you should see the following output:

```console
VITE v3.2.5 ready in 238 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
```

Open the URL [http://localhost:5173/](http://localhost:5173/) in a browser, and you should see something similar to the screenshot below.
![proformajs-vue_start.png](assets%2Fproformajs-vue_start.png)

## Load starter model in proformajs-vue

- Copy and paste the contents in [starter_model.json](https://github.com/gopi-kris/proforma_starter_project/blob/main/assets/starter_model.json) file to the Code section of
  proformajs-vue.
- Click Review to execute the model.
  ![json_code.png](assets%2Fjson_code.png)

## Exit proformajs-vue

- CTRL+C in the terminal to exit proformajs-vue.