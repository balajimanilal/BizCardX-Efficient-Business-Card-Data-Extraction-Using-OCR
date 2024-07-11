# BizCardX-Efficient-Business-Card-Data-Extraction-Using-OCR

The code is a Streamlit-based code designed to manage business card information efficiently. It allows users to upload, extract, display, modify, and delete details from a PostgreSQL database. Here are the key functionalities:

**Initial Setup and Configuration**
* Importing Libraries: The code imports various libraries for image processing (easyocr and PIL), database operations (pandas and sqlalchemy), and building the web application (streamlit and streamlit_option_menu).
* Database Connection: Establishes a connection to a PostgreSQL database using SQLAlchemy. The business_card table schema is reflected and accessed for subsequent operations.

**Text Extraction Function**
extract_text(image_path): Uses EasyOCR to read text from an image file (business card) and returns the extracted text details as a list.

**Text Processing Function**
process_text(details): Processes the extracted text details, categorizing them into fields such as name, designation, contact, email, website, address, etc. Uses regular expressions to match and extract relevant information.

**Storing Data**
store_data(data): Converts the processed data into a DataFrame and stores it in the business_card table in the PostgreSQL database.

**Streamlit Web Interface**
* Page Configuration: Configures the Streamlit page with a title, icon, and layout.
* Main Menu: Provides a main menu with options: Home, Upload, and Database.

**Home Section**
* Displays an introductory message and description of the app.
* Provides information about the app's purpose and the technologies used.

**Upload Section**
* File Uploader: Allows users to upload an image file (business card).
* Image Display: Displays the uploaded image.
* Extract and Upload Buttons: Buttons to extract text from the image and upload the extracted details to the database.
* Instruction Box: Provides instructions for uploading and processing the image.

**Database Section**
* Displays the current data stored in the business_card table.
* Provides sub-menu options to Modify or Delete data.

**Modify Data**
* Allows users to select a category (name, contact, email) and specific details within that category to modify.
* Prompts for new values and commits changes to the database.

**Delete Data**
* Allows users to select a category (name, email) and specific details within that category to delete.
* Confirms the deletion and executes the delete operation, committing changes to the database.

---

**Technologies Used**
Python: Core programming language used for development.
Streamlit: Web application framework used for building the user interface.
EasyOCR: Optical Character Recognition library used for extracting text from images.
Pandas: Data manipulation library used for processing and organizing extracted information.
SQLAlchemy: SQL toolkit and Object-Relational Mapping (ORM) library used for database operations.
PostgreSQL: Relational database management system used for storing business card information.

---

> **Summary of Functionality**
* Extracting Information: Uses OCR to extract text from business card images.
* Processing Data: Categorizes and processes the extracted text.
* Database Operations: Stores, modifies, and deletes business card details in a PostgreSQL database.
* User Interface: Provides a user-friendly interface for interacting with the app, including file upload, data display, and database management.
* This is designed to help users manage business card information efficiently, leveraging OCR for text extraction and Streamlit for a seamless web interface experience.
