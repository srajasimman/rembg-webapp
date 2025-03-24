# ✂️ rmbg - Remove Background from Images

`rmbg` is a simple web application that allows users to upload an image and remove its background using the `rembg` library. The processed image can then be downloaded with the background removed.

## Features

- Drag-and-drop or file upload support.
- Automatic background removal using AI.
- Download the processed image in PNG format.

## Requirements

- Python 3.8 or higher
- The following Python libraries (listed in `requirements.txt`):
  - Flask
  - rembg[cpu]
  - Pillow
  - gunicorn

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/srajasimman/rmbg.git
   cd rmbg
   ```

2. Create a virtual environment and activate it:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Start the application:
   ```bash
   python app.py
   ```

2. Open your browser and navigate to `http://localhost:5100`.

3. Drag and drop an image or use the file input to upload an image.

4. The application will process the image and provide a download link for the background-removed image.

## Deployment

To deploy the application using Gunicorn:

1. Run the following command:
   ```bash
   gunicorn -c gunicorn.conf.py app:app
   ```

2. The application will be available at `http://0.0.0.0:5100`.

## File Structure

```
rmbg/
├── app.py                # Main Flask application
├── gunicorn.conf.py      # Gunicorn configuration
├── requirements.txt      # Python dependencies
├── templates/
│   └── index.html        # HTML template for the web interface
└── README.md             # Project documentation
```

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

## Acknowledgments

- [rembg](https://github.com/danielgatis/rembg) for the background removal functionality.
- [Flask](https://flask.palletsprojects.com/) for the web framework.
