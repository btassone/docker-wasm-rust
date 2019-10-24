# Docker WASM Rust

Docker container for developing WASM-Rust applications.

Technologies installed right out of the box

* rust
* cargo
* cargo-generate
* wasm-pack
* npm
* yarn
* nginx

Technologies / alternate tagged containers planned for the future

* MySQL

# Usage

### Docker Compose

1. Create a docker-compose.yml file (example below)

**Example: docker-compose.yml**

```yml
version: '3.7'
services:
  rust:
    image: btassone/wasm-rust
    ports:
      - 8080:80
    volumes:
      - ./project:/var/www/html/project
volumes:
  rust:
```

2. docker-compose up -d
3. docker exec -it [docker pid goes here] /bin/bash
4. cd /root/project
5. cargo build / run

# Next Steps

If you are new to WASM Rust and are looking for further steps to get started
please take a look at:

https://rustwasm.github.io/
