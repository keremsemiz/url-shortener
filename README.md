# URL Shortener API

This is a simple FastAPI-based API for shortening URLs. It provides endpoints to shorten a URL and resolve a shortened URL back to its original form.

## Features

- **Shorten URL**: Convert a long URL into a shortened version.
- **Resolve URL**: Retrieve the original URL from the shortened version.

## Installation

### Using Poetry

1. Clone the repository:
    ```bash
    git clone https://github.com/keremsemiz/url-shortener.git
    cd url-shortener-api
    ```

2. Install dependencies:
    ```bash
    poetry install
    ```

3. Run the application:
    ```bash
    poetry run uvicorn url_shortener_api.main:app --reload
    ```

### Using Pip

1. Clone the repository:
    ```bash
    git clone https://github.com/keremsemiz/url-shortener.git
    cd url-shortener-api
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the application:
    ```bash
    uvicorn url_shortener_api.main:app --reload
    ```

## Usage

After starting the application, you can interact with the API at `http://127.0.0.1:8000`.

### Endpoints

- **POST /shorten/**: Shorten a long URL.
  - Request Body: `{ "url": "https://example.com/very/long/url" }`
  - Response: `{ "original_url": "https://example.com/very/long/url", "shortened_url": "/abc123" }`

- **GET /{short_url}**: Resolve a shortened URL to its original form.
  - Example: `GET /abc123`
  - Response: `{ "original_url": "https://example.com/very/long/url", "shortened_url": "/abc123" }`

You can also explore the API documentation by visiting `http://127.0.0.1:8000/docs` in your browser.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
