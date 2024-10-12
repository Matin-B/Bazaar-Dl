# Bazaar-Dl

Simple Python package for directly downloading applications from Cafe Bazaar (cafebazaar.ir).

## Installation

Install the package using pip:
```sh
pip install Bazaar-Dl
```

## Example Usage

To download an app by its package name:
```python
from bazaar_dl import download

# Download an application from Cafe Bazaar
result = download("com.android.chrome")
print(result)
```

### Sample Output

For a successful download:
```python
{'status': 'success',
 'status_code': 200,
 'data': {'download_link': 'https://appcdn2.cafebazaar.ir/apks/411684004063.apk?expire=1729014711&token=1968a55c45e145e64eb90f4653644462&a=.apk',
  'package_size': '48667070',
  'installation_size': '73000605'}}
```

For an error (e.g., invalid package name):
```python
{'status': 'error',
 'status_code': 404,
 'message': '{"properties":{"statusCode":404,"errorMessage":"متأسفانه برنامه مورد نظر شما یافت نشد."},"singleReply":null}'}
```

### Notes
- Replace `"com.android.chrome"` with the package name of the application you want to download.

