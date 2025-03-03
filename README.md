# Simple Encryption and Decryption Tool

## Objective
The Simple Encryption and Decryption Tool is a Python-based application that provides symmetric encryption and decryption functionalities using the `cryptography` library. The tool allows users to securely encrypt plaintext data, save encrypted data to a file, and later decrypt the data when needed.

## Features
- Generate and store a secure encryption key
- Encrypt plaintext data
- Decrypt encrypted data
- Save encrypted data to a file
- Load encrypted data from a file
- User-friendly command-line menu

## Requirements
Ensure you have Python installed on your system. The tool requires the `cryptography` package. You can install it using:
```sh
pip install cryptography
```

## Installation and Setup
1. Clone or download the script to your local system.
2. Install the required dependencies using `pip install cryptography`.
3. Run the script using:
```sh
python encryption_tool.py
```

## How to Use
Upon running the script, the following options will be available:

1. **Generate Key**
   - Generates a new encryption key and saves it as `secret.key`.
   
2. **Encrypt Data**
   - Loads the existing key.
   - Asks the user for plaintext input.
   - Encrypts the plaintext and displays the encrypted output.
   
3. **Decrypt Data**
   - Loads the existing key.
   - Prompts the user to provide the filename containing the encrypted data.
   - Decrypts and displays the original plaintext if the correct key is used.
   
4. **Save Encrypted Data to File**
   - Loads the existing key.
   - Encrypts user-provided plaintext.
   - Saves the encrypted data to a specified file.
   
5. **Load Encrypted Data from File**
   - Prompts the user for the filename containing the encrypted data.
   - Displays the encrypted data in its raw form.
   
6. **Exit**
   - Exits the program.

## Code Explanation
- `generate_key()`: Creates and saves a secure key for encryption.
- `load_key()`: Retrieves the key from `secret.key`.
- `encrypt_data(plaintext, key)`: Encrypts a plaintext message.
- `decrypt_data(ciphertext, key)`: Decrypts an encrypted message.
- `save_encrypted_data(filename, encrypted_data)`: Saves encrypted content to a file.
- `load_encrypted_data(filename)`: Loads encrypted data from a file.
- `main()`: Provides an interactive command-line interface for users.

## Example Usage
```sh
Select an option: 1
Key generated and saved as 'secret.key'

Select an option: 2
Enter plaintext: Hello World!
Encrypted Data: gAAAAABi...

Select an option: 4
Enter filename to save encrypted data: secure.txt
Encrypted data saved to secure.txt

Select an option: 3
Enter filename to load encrypted data from: secure.txt
Decrypted Data: Hello World!
```

## Notes
- If the `secret.key` file is lost, previously encrypted data cannot be recovered.
- The same key must be used for both encryption and decryption.
- Ensure that the key file remains secure and is not shared.

## License
This project is open-source and available for educational and personal use.

