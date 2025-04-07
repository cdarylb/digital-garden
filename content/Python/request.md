```python
import requests
import time

URL = "https://www.rudeops.com"

def check_website(url):
    try:
        print(f"🔍 Checking {url} ...")
        start = time.time()
        response = requests.get(url, timeout=5)
        end = time.time()
        response_time = round((end - start) * 1000, 2)  # en ms

        print("Site is UP")
        print(f"Status Code: {response.status_code}")
        print(f"Response Time: {response_time} ms")

    except requests.exceptions.Timeout:
        print("Timeout: The server took too long to respond.")
    except requests.exceptions.ConnectionError:
        print("Connection Error: Site is fucked or unreachable.")
    except Exception as e:
        print(f"Unexpected error: {e}")

if __name__ == "__main__":
    check_website(URL)
