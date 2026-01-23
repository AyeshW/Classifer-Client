# Classifer Client

A JavaFX-based desktop application for document classification. This application provides a client interface for uploading and classifying documents using machine learning classifiers.

## Features

- **User Authentication**: Secure login system with password hashing using BCrypt
- **User Management**: Support for multiple user types (Admin and Client)
- **Document Analysis**: Upload and analyze documents (PDF files) using machine learning classifiers
- **Admin Panel**: Administrative interface for user management
- **Settings**: Customizable application settings
- **SQLite Database**: Local database for storing user data and application state

## Prerequisites

- Java Development Kit (JDK) 8 or higher with JavaFX support
- SQLite JDBC driver
- Apache PDFBox library
- BCrypt library for password hashing
- JSON library

## Dependencies

The application uses the following libraries:

- **sqlite-jdbc-3.23.1**: SQLite database connectivity
- **jbcrypt-0.3m**: Password hashing
- **Apache PDFBox 2.0.15**: PDF file processing
  - fontbox-2.0.15.jar
  - pdfbox-2.0.15.jar
  - pdfbox-tools-2.0.15.jar
  - preflight-2.0.15.jar
  - xmpbox-2.0.15.jar
- **json-20180813**: JSON processing
- **commons-io-2.6**: Apache Commons IO utilities
- **JUnit 4.12 & JUnit 5**: Testing framework

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AyeshW/Classifer-Client.git
   ```

2. Open the project in your IDE (IntelliJ IDEA recommended)

3. Ensure all dependencies are properly configured in your project

4. Build the project

## Usage

1. Run the `Main.java` class located in the `classifer` package

2. The application will start with the login screen

3. Log in with your credentials:
   - Admin users can access the admin panel
   - Regular users can access the client interface

4. **For Clients**:
   - Upload documents using the file chooser
   - Select a classifier type (Generic or Confidential)
   - Analyze the documents
   - View classification results

5. **For Admins**:
   - Manage user accounts
   - View user data
   - Configure application settings

## Project Structure

```
Classifer-Client/
├── src/
│   ├── admin/           # Admin panel interface and user management
│   ├── analyzer/        # Document analysis logic
│   ├── classifer/       # Main application entry point
│   ├── client/          # Client interface for document upload and analysis
│   ├── dbUtil/          # Database connection utilities
│   ├── fileHandler/     # File reading and opening functionality
│   ├── logginApp/       # Login interface and authentication
│   ├── setting/         # Application settings
│   ├── signUp/          # User registration
│   └── Tests/           # Unit tests
├── Classifer.sqlite     # SQLite database file
└── ClassiferFx.iml      # IntelliJ IDEA module file
```

## Technologies Used

- **JavaFX**: UI framework for building the desktop application
- **SQLite**: Lightweight database for local data storage
- **Apache PDFBox**: PDF processing and text extraction
- **BCrypt**: Secure password hashing
- **JSON**: Data exchange format for communication with classifiers
- **JUnit**: Unit testing framework

## Development

To run the tests:

```bash
# Run unit tests using your IDE's test runner
# Test classes are located in src/Tests/
```

## License

This project is part of an academic or personal project. Please check with the repository owner for licensing information.

## Contributors

- AyeshW (Repository Owner)

## Notes

- The application connects to a classifier service via HTTP to perform document classification
- PDF files are processed and their text content is extracted for analysis
- User passwords are securely hashed using BCrypt before storage
