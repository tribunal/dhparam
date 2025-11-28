# dhparam

A collection of pre-calculated Diffie-Hellman parameters (dhparam) for testing and development purposes.

## ⚠️ Important Warning

> **DO NOT USE IN A PRODUCTION ENVIRONMENT.**
>
> These keys are public and pre-generated. Using them in production significantly compromises the security of your cryptographic handshake. They are intended **strictly for testing, staging, or local development environments** where speed is prioritized over security.

## Contents

This repository contains Diffie-Hellman parameters in the following bit lengths:

* **1024 bit** (Fastest generation, lowest security)
* **2048 bit** (Standard for many legacy systems)
* **3072 bit** (Stronger security)
* **4096 bit** (Highest security, slowest generation)

## Usage

You can download a specific parameter file directly using `wget` or `curl`:

```bash
# Example: Download 2048-bit params
wget [https://raw.githubusercontent.com/tribunal/dhparam/main/2048/dhparam.pem](https://raw.githubusercontent.com/tribunal/dhparam/main/2048/dhparam.pem)
```

Then reference the file in your server configuration (e.g., Nginx):

```nginx
ssl_dhparam /path/to/dhparam.pem;
```

