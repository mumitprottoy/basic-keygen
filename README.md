# 🔐 KeyGen - Secure Random Key Generator

`keygen.py` is a simple, secure Python module that generates unique, cryptographically secure keys and IDs. It’s perfect for creating transaction identifiers, OTPs, verification codes, and any use case requiring non-predictable strings.

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
from keygen import KeyGen

kg = KeyGen()

# Generate a 6-digit OTP or numeric verification code
print(kg.num_key())  # Example: '804219'

# Generate a 4-character alphabetic key
print(kg.alpha_key(key_len=4))  # Example: 'XrTp'

# Generate an 8-character alphanumeric key
print(kg.alphanumeric_key(key_len=8))  # Example: 'A3d9Fg7Q'

# Generate a timestamped alphanumeric ID (good for filenames or short IDs)
print(kg.timestamped_alphanumeric_id(head_len=5))  # Example: 'aB9QX120515051234'

# Generate a full transaction ID with optional prefix and random suffix
print(kg.transaction_id(head='TXN', tail_len=4))  # Example: 'TXN120515051234PQ9D'

# Generate a datetime string key (microsecond precision)
print(kg.datetime_key())  # Example: '120515051234'
