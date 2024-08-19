# File Metadata Microservice

This is a File Metadata Microservice project built as part of the [freeCodeCamp Back End Development and APIs Certification](https://www.freecodecamp.org/learn/back-end-development-and-apis/back-end-development-and-apis-projects/file-metadata-microservice).

## Project Overview

The File Metadata Microservice allows users to upload files and receive metadata about those files. This is particularly useful for extracting details like file size from uploaded files.

### Features

- **File Upload**: Upload files via a form or API request.
- **Metadata Extraction**: Get metadata such as file size for the uploaded files.
- **Error Handling**: Handles file uploads and returns appropriate error messages for invalid requests.

## API Endpoints

### POST `/api/fileanalyse`

- **Request**: 
  - **Content-Type**: `multipart/form-data`
  - **Form Data**: `upfile` (The file to be uploaded)

- **Response**: 
  ```json
  {
    "name": "filename.ext",
    "type": "filetype",
    "size": filesize
  }
  ```

  Where:
  - `name` is the name of the file.
  - `type` is the MIME type of the file.
  - `size` is the size of the file in bytes.

## How to Run

1. **Clone the Repository**

   ```bash
   git clone https://github.com/amittannagit/FCC-File-Metadata-Microservice.git
   cd FCC-File-Metadata-Microservice
   ```

2. **Install Dependencies**

   ```bash
   npm install
   ```

3. **Set Up Environment Variables**

   Ensure you have a `.env` file in the root of the project. This file can be empty if there are no specific environment variables required.

4. **Run the Application**

   ```bash
   npm start
   ```

   The application will start on port 3000 or the port specified in your `.env` file.

## Project Structure

- `index.js` - Main server file.
- `views/index.html` - HTML file for the frontend (if any).
- `public/` - Public directory for static files.
- `.env` - Environment variables file.

## Testing

To test the application, use tools like [Postman](https://www.postman.com/) or `curl` to make POST requests to `/api/fileanalyse` with a file.

Example `curl` command to test the file upload:

```bash
curl -F "upfile=@path/to/your/file" http://localhost:3000/api/fileanalyse
```

## Contributing

Feel free to submit issues or pull requests to improve this project. 

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
