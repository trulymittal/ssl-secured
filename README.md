## How to use SSL/TLS certificates in NodeJS express applications

This repo demonstrates how to use a ssl/tls certificate to be used in a nodejs express application for development purposes.

---

## To start setting up the project

Step 1: Clone the repo

```bash
git clone https://github.com/trulymittal/ssl-secured.git
```

Step 2: cd into the cloned repo and run:

```bash
npm install
```

Step 3(optional): Incase nodemon NOT installed globally on system.

```bash
npm install -g nodemon
```

Step 4: Switch to _cert/_ directory

```bash
cd cert/
```

Step 5. Generate SSL/TLS certificates (valid for 365 days)

```zsh
openssl genrsa -out key.pem

openssl req -new -key key.pem -out csr.pem

openssl x509 -req -days 365 -in csr.pem -signkey key.pem -out cert.pem
```

## Author

- [**Truly Mittal**](https://trulymittal.com)

## Contribute

You can fork this repo and send me a PR.

## License

This project is licensed under the MIT License.
