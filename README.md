# 🔐 csharp-encryption

A C# library for experimenting with and implementing various encryption and data-hiding techniques, including modern cryptographic algorithms and steganography. This repo is ideal for developers, students, and security enthusiasts interested in learning how different methods work under the hood — all through clean, reusable C# code.

---

## 🚀 Features

- 📦 Modular implementations for:
  - **AES** (Advanced Encryption Standard)
  - **PGP** (Pretty Good Privacy-style hybrid encryption)
  - **Steganography** (data hiding in images)
  - **RSA** (Asymmetric encryption)
  - **Base64 and XOR** (for simple encoding and obfuscation)

- 🔁 Unified interface for encrypting/decrypting across modules
- 📚 Well-documented examples for each encryption type
- 🧪 Unit-test ready structure for validating encryption/decryption
- 🌐 .NET Standard-compatible

---

## 📁 Project Structure

```bash
csharp-encryption/
├── EncryptionCore/         # Core interfaces and utilities
├── AES/                    # AES keygen + encrypt/decrypt
├── RSA/                    # RSA keypair generation and usage
├── PGP/                    # PGP-style hybrid encryption
├── Steganography/          # Image-based encoding/decoding
├── Tests/                  # NUnit or xUnit test cases
├── Examples/               # Console demos for each method
└── README.md
```

🛠️ Usage
AES Example

```csharp
var aes = new AesEncryption();
var key = aes.GenerateKey();
string encrypted = aes.Encrypt("Top Secret Message", key);
string decrypted = aes.Decrypt(encrypted, key);
```

RSA Example
```csharp
var rsa = new RsaEncryption();
rsa.GenerateKeys(out string publicKey, out string privateKey);
string encrypted = rsa.Encrypt("Confidential", publicKey);
string decrypted = rsa.Decrypt(encrypted, privateKey);
```

Steganography Example
```csharp
var steg = new ImageSteganography();
steg.EmbedMessage("cover.png", "Hidden text", "output.png");
string message = steg.ExtractMessage("output.png");
```
📦 Installation
Clone the repo and open in Visual Studio or VS Code:
```bash
git clone https://github.com/your-username/csharp-encryption.git
cd csharp-encryption
```

Then build the solution. Projects are modular and can be used independently.

🧩 Contributing
Got an encryption algorithm you'd like to add (e.g., Blowfish, ChaCha20, One-Time Pad)? PRs are welcome! Please follow the structure used in existing modules and include a usage example + test case.

📄 License
MIT License — free to use, modify, and distribute.

👨‍💻 Author
Bernard Lawes
Security-aware software architect & AI/Computer Vision specialist
Connect with me on LinkedIn






