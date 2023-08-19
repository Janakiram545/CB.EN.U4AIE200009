
## FastAPI Number Management Microservice

This microservice, built using FastAPI, fetches numbers from multiple URLs and returns unique numbers in ascending order.

### Features

- **Caching**: Responses from URLs are cached for better performance.
- **Timeout**: URLs are fetched within 500ms; slow URLs are ignored.
- **Concurrency**: Concurrent requests enhance efficiency.

### Setup

1. Install dependencies:

   ```bash
   pip install fastapi requests cachetools
   ```

2. Start the server:

   ```bash
   uvicorn app:app
   ```

### Usage

Send GET requests to `http://localhost:8008/numbers?url=url1&url=url2`.

### Notes

- Assumes each URL returns JSON with "numbers".
- Caching optimizes performance.
- Adjust timeouts and concurrency as needed.