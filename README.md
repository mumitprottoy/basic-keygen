# 🔐 KeyGen - Secure Random Key Generator

`keygen.py` is a simple, secure Python module designed to generate unique, cryptographically secure keys and IDs. It’s perfect for creating transaction identifiers, OTPs, verification codes, and any use case where non-predictable strings are required.

---

## 🚀 Features

- ✅ Cryptographically secure randomness via `secrets`
- 🕒 Timestamp-based uniqueness for traceability
- 🔢 Generates numeric, alphabetic, and alphanumeric keys
- 🧾 Built-in transaction ID generator
- 🔐 OTP and verification code generator
- ⚙️ Easily extensible and dependency-free

---

## 📦 Installation

No external dependencies required!

Simply clone or download `keygen.py`:

---

## 📚 Usage

```bash
git clone https://github.com/yourusername/keygen.git

from keygen import KeyGen

kg = KeyGen()

# Generate a 6-digit OTP (numeric code)
print(kg.num_key())  # Example: '842613'

# Generate a random alphabetic key (e.g., for temporary names)
print(kg.alpha_key(5))  # Example: 'pQwEr'

# Generate a random alphanumeric key
print(kg.alphanumeric_key(8))  # Example: 'R3t8Wq9Z'

# Generate a secure key with embedded timestamp
print(kg.key())  # Example: 'QM9xT5194210509273512'

# Generate a transaction ID
print(kg.transaction_id())  # Example: 'TXN194210509273512XF8A'

# Generate a unique username or identifier
print(kg.unique_name())  # Example: 'D4r8B194210509273512'
