A secure, local password management system built with Python that helps you store and manage your passwords safely using military-grade encryption.

🌟 Features
🔒 Military-Grade Encryption: AES-256 encryption for all stored data

🎯 Strong Password Generator: Generate secure random passwords

📊 Password Strength Evaluation: Check how strong your passwords are

🔍 Smart Search: Find passwords by website or category

📁 Category Organization: Organize passwords by categories

💾 Local Storage: Your data never leaves your computer

🛡️ Master Password: Single secure password to access all your data

🚀 Quick Start
Prerequisites
Python 3.6 or higher

pip package manager

Installation
Clone or download the project files

bash
# If using git
git clone <repository-url>
cd password-manager
Install required dependencies

bash
pip install -r requirements.txt
Run the application

bash
python password_manager.py
First-Time Setup
Create Master Password

text
Welcome! Let's setup your Password Manager.
=== Setup Master Password ===
Create master password: ********
Confirm master password: ********
Master password setup successfully!
Start Managing Passwords

Add your first password entry

Generate strong passwords

Organize by categories

📖 How to Use
Adding a New Password
Select option 1 from main menu

Enter website/app name

Enter username/email

Choose to generate or enter password

Add optional category and notes

Viewing Passwords
Option 2: View all passwords (passwords masked for security)

Option 3: View specific password details

Option 4: Search passwords by website or category

Generating Strong Passwords
Option 5: Generate random secure passwords

Customizable length (minimum 8 characters)

Includes letters, numbers, and special characters

Managing Entries
Option 6: Delete password entries

All changes are automatically encrypted and saved

🛡️ Security Features
Encryption
AES-256 symmetric encryption

PBKDF2 key derivation with 100,000 iterations

Fernet tokens for secure encryption

Random salt generation for each installation

Data Protection
Master password never stored in plain text

All data encrypted before saving to disk

Local storage only - no cloud synchronization

Secure password masking in console

Password Security
Strength evaluation algorithm

Strong password generation

No password length limitations

Special character support

📁 Project Structure
text
password-manager/
├── password_manager.py    # Main application
├── requirements.txt       # Python dependencies
├── README.md             # This file
├── passwords.enc         # Encrypted password database (auto-created)
├── key.key              # Encryption keys (auto-created)
├── /screenshots         # Application screenshots
│   ├── main_menu.png
│   ├── add_password.png
│   └── view_passwords.png
└── /recordings          # Demo recordings
    └── demo.mp4
🔧 Technical Details
Built With
Python 3 - Core programming language

cryptography - Encryption library

JSON - Data serialization

Modules
Authentication - Master password handling

Encryption - AES-256 implementation

Password Generator - Secure random generation

Data Manager - File I/O operations

UI Controller - Command-line interface

Security Implementation
python
# Key derivation
kdf = PBKDF2HMAC(
    algorithm=hashes.SHA256(),
    length=32,
    salt=salt,
    iterations=100000,
)

# Encryption
fernet = Fernet(key)
encrypted_data = fernet.encrypt(data)
🎯 Course Alignment
This project demonstrates:

✅ Real-World Problem Solving: Addresses password security challenges
✅ Structured Development: Follows software engineering principles
✅ Technical Skills: Encryption, file I/O, OOP, data structures
✅ Professional Tools: GitHub, documentation, version control

Development Process
Problem Definition: Password security management

Requirements Analysis: Security, usability, functionality

Modular Design: Separate components for each functionality

Algorithm Development: Encryption, password generation

Implementation: Python code with security best practices

Testing & Refinement: Comprehensive testing and validation

⚠️ Important Security Notes
Never share your master password

Keep your key.key file secure - losing it means losing access to your data

Regularly backup your passwords.enc file

This is a learning project - consider professional password managers for critical use

🐛 Troubleshooting
Common Issues
"ModuleNotFoundError: No module named 'cryptography'"

bash
pip install cryptography
"Invalid master password"

Ensure caps lock is off

Check for typos

If lost, delete key.key and passwords.enc to start over (⚠️ data loss)

File permission errors

Run as administrator if needed

Check file/folder permissions

🤝 Contributing
Fork the project

Create a feature branch

Commit your changes

Push to the branch

Open a Pull Request

📄 License
This project is created for educational purposes as part of academic coursework.

👨‍💻 Developer
Created as a course project demonstrating Python programming, security principles, and software development methodologies.

🔒 Your Security Matters: This password manager keeps your data encrypted and local. You control your passwords completely!# Password-Manager
