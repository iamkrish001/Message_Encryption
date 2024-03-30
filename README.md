**README.md**

# Message Encryptor

This Python script demonstrates a basic message encryptor using the AES256 encryption algorithm. The script allows for encrypting and decrypting messages exchanged between users.

## How it Works

The script simulates a messaging system between two users, Krish and Sangit. Here's a breakdown of how it operates:

1. **Message Data Structure**: The messages exchanged between Krish and Sangit are stored in a dictionary named `message_data`. Each user has a list of dictionaries containing messages along with their corresponding timestamps.

2. **Encryption and Decryption Functions**: The script utilizes the `cryptography` library to implement encryption and decryption functionalities. The `encrypt_message()` function encrypts a given message using AES256 encryption, while the `decrypt_message()` function decrypts a given ciphertext using the same encryption key.

3. **Encryption Process**: During encryption, each message is encrypted using a randomly generated Initialization Vector (IV) and a shared secret key (`shared_secret_key`). The IV is prepended to the ciphertext for later use in decryption.

4. **Decryption Process**: During decryption, the IV is separated from the ciphertext. Using the shared secret key and the IV, the ciphertext is decrypted to retrieve the original plaintext message.

5. **Message Data Manipulation**: The script iterates through each message in the `message_data` dictionary, encrypts the messages, and updates the dictionary with the encrypted messages represented in hexadecimal format. After encryption, the script decrypts the messages to ensure the integrity of the encryption process.

## Usage

To use this script:

1. Ensure you have Python installed on your system.

2. Install the `cryptography` library using pip:
   ```
   pip install cryptography
   ```

3. Copy and paste the provided Python script into your Python environment.

4. Run the script. It will output the encrypted and decrypted message data dictionaries to the console.

## Note

This script is intended for educational purposes and demonstrates a basic implementation of message encryption. It may not be suitable for production environments without further enhancements and security considerations.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to contribute to and enhance this project. If you encounter any issues or have suggestions for improvement, please open an issue or submit a pull request.
