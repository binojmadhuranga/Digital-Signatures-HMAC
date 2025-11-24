# Digital Signatures & HMAC

A Python implementation demonstrating digital signatures using RSA encryption and Message Authentication Codes (HMAC) for secure message authentication and integrity verification.

## 📋 Overview

This project implements cryptographic techniques for:
- **Digital Signatures**: Sign and verify messages using RSA public-key cryptography
- **HMAC**: Generate and verify message authentication codes using shared secret keys

## 🔧 Prerequisites

- Python 3.x
- `pycryptodome` library

## 📦 Installation

1. Clone or download this repository

2. Install the required dependencies:
```bash
pip install pycryptodome
```

## 🚀 Usage

Run the program:
```bash
python crypto.py
```

### Features

The program provides an interactive menu with the following options:

#### 1. Generate and Sign a Message (Digital Signature)
- Generates a 2048-bit RSA key pair (private and public keys)
- Signs a message using the private key
- Outputs the signature in Base64 encoding
- Use the public key to verify the signature later

#### 2. Verify a Digital Signature
- Verifies a previously signed message
- Requires the public key, original message, and signature
- Confirms message authenticity and integrity

#### 3. Generate and Verify HMAC
- Creates a message authentication code using SHA-256
- Uses a shared secret key for authentication
- Verifies message integrity

#### 4. Exit
- Exits the program

## 🔐 Security Features

- **RSA-2048**: Uses 2048-bit RSA keys for strong security
- **SHA-256**: Implements SHA-256 hashing algorithm
- **PKCS#1 v1.5**: Uses PKCS#1 v1.5 signature scheme
- **Base64 Encoding**: Signatures are encoded in Base64 for easy transmission

## 📖 How It Works

### Digital Signatures
1. A message is hashed using SHA-256
2. The hash is encrypted with the sender's private key (signing)
3. The receiver decrypts the signature with the sender's public key (verification)
4. If the decrypted hash matches the message hash, the signature is valid

### HMAC (Hash-based Message Authentication Code)
1. A secret key is shared between sender and receiver
2. The message and key are combined and hashed using SHA-256
3. The receiver can verify the message by regenerating the HMAC with the same key

## 🎓 Educational Purpose

This project was developed for **Computer and Network Security - Practical 7** to demonstrate:
- Public-key cryptography concepts
- Digital signature creation and verification
- Message authentication techniques
- Practical cryptographic implementations in Python

## ⚠️ Disclaimer

This implementation is for educational purposes. For production use, consider:
- Using established cryptographic libraries with proper security audits
- Implementing proper key management systems
- Following current security best practices and standards

## 📝 License

This project is open source and available for educational use.

