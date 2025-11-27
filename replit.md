# Securing Cloud Storage Using Homomorphic Encryption

## Overview
This is a Python CLI application that demonstrates secure cloud storage using homomorphic encryption. The application takes a text file, encrypts it using TenSEAL's CKKS homomorphic encryption scheme, compresses it, and uploads it to Dropbox.

## Purpose
The project showcases how to:
- Convert text files to ASCII format
- Apply homomorphic encryption to protect data privacy
- Compress encrypted files to reduce storage size
- Upload encrypted data to cloud storage (Dropbox)

## Project Architecture

### Main Components
- **ASCII Conversion**: Converts input text to ASCII values for processing
- **Homomorphic Encryption**: Uses TenSEAL library with CKKS scheme for encryption
- **Compression**: GZIP compression to reduce file size
- **Cloud Upload**: Dropbox integration with retry logic for reliable uploads

### Technology Stack
- **Language**: Python 3.11
- **Package Manager**: UV (modern Python package manager)
- **Key Dependencies**:
  - `tenseal`: Homomorphic encryption library
  - `dropbox`: Dropbox SDK for file uploads
  - `retrying`: Retry decorator for network operations
  - `numpy`: Required by TenSEAL

## How to Use

1. Run the application from the Replit console
2. Provide the path to a text file when prompted
3. Enter your Dropbox access token when requested
4. The application will:
   - Convert the file to ASCII
   - Encrypt it using homomorphic encryption
   - Compress the encrypted file
   - Upload to your Dropbox account

## File Structure
```
.
├── Securing Cloud Storage Using Homomorphic Encryption.py  # Main application
├── .gitignore                                              # Git ignore patterns
├── pyproject.toml                                          # Python dependencies
└── replit.md                                               # This documentation
```

## Generated Files
The application creates temporary files during execution:
- `output_ascii.txt`: ASCII representation of input file
- `encrypted_output.txt`: Encrypted data
- `encrypted_output.txt.gz`: Compressed encrypted file (uploaded to Dropbox)

These files are gitignored to prevent committing sensitive data.

## Recent Changes
- **2025-11-27**: Initial import and setup in Replit environment
  - Installed Python 3.11 and all dependencies
  - Added numpy dependency (required by tenseal)
  - Created .gitignore for Python project
  - Configured workflow to run the application
  - Created project documentation

## Notes
- The application requires a valid Dropbox access token
- Encrypted files use CKKS homomorphic encryption scheme (allows operations on encrypted data)
- Network operations include retry logic for reliability
