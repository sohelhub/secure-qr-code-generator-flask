# secure-qr-code-generator-flask
A Python Flask web application that encrypts URLs and text using symmetric cryptography and generates scannable QR codes with built-in decryption.

# Secure QR Code Generator Web Application

A Python full-stack web application built with **Flask** and **symmetric cryptography** that encrypts sensitive URLs or text payloads before encoding them into scannable QR codes, with built-in decryption support.

## Features

- **Payload Encryption:** Encrypts user-submitted URLs and text messages using symmetric encryption (`cryptography` / Fernet) so sensitive data is never exposed in plaintext inside the QR code.
- **Dynamic QR Code Generation:** Converts encrypted ciphertext into high-contrast, downloadable QR code images using Python's `qrcode` and `Pillow` libraries.
- **Built-in Decryption:** Allows authorized users to submit the encrypted payload or scanned QR string back through the web interface to recover the original message.
- **Responsive Web Interface:** Clean, lightweight frontend built with HTML5, CSS3, and Jinja2 templates for seamless use across desktop and mobile browsers.

## Tech Stack

- **Backend:** Python 3, Flask
- **Security & Encoding:** `cryptography` (Fernet symmetric encryption), `qrcode`, `Pillow`
- **Frontend:** HTML5, CSS3, Jinja2 Templates

## Project Structure

```text
secure-qr-code-generator-flask/
├── app.py               # Main Flask application, encryption/decryption routes, and QR generation logic
├── requirements.txt     # Python dependencies
├── templates/           # Jinja2 HTML templates for the UI
└── static/              # Stylesheets and static assets
