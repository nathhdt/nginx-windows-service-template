# nginx-windows-service-template

lightweight template for packaging nginx as a Windows service

## overview

this project provides a simple structure to package, install, and run an nginx instance as a native Windows service with a standard Windows installer experience.

## project structure

```text
├── cmd/
│   ├── WinSW.exe
│   └── service configuration files
│
├── nginx/
│   ├── nginx.exe
│   ├── conf/
│   ├── logs/
│   └── ...
│
├── web/
│   └── website files served by nginx
│
├── setup.iss
│
└── README.md
```

## nginx preparation

this repository does not include nginx binaries. download nginx from the [official website](https://nginx.org/en/download.html).

extract the downloaded archive into the `nginx/` directory.

## web files

the `web/` directory contains the static files served by nginx. replace these files with your own content.

## installer build

open `setup.iss` with Inno Setup and compile the installer.

## dependencies

- Inno Setup
- WinSW
- nginx for Windows