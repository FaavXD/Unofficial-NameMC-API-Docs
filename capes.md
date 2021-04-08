# NameMC Capes API docs
NameMC has their own system for caching capes.

This API's purpose is to get all capes a user owns according to NameMC.

### `GET /v1/namemc/capes?username=:IGN_Here`
This is the only endpoint for this API.

Parameters are as follows:
- **`IGN_Here`** - the current username of the account

### Possible responses

The API will almost always return HTTP status code `200 OK` and set its `Content-Type` header to `application/json`.

If the user you provide doesn't exist, the API will return HTTP status code `404 Not Found`, and the `Content-Type` header will remain `application/json`.

Here are the different responses that can be returned:

**Returns the users Capes / HTTP `200`:**
```json
[{"hash":"ebc798c3f7eca2a3","name":"MineCon 2012","raw":"https:\/\/texture.namemc.com\/eb\/c7\/ebc798c3f7eca2a3.png","url":"https:\/\/namemc.com\/cape\/ebc798c3f7eca2a3"}]
```

**No Capes / HTTP `200`:**
```json
[]
```

**You Didn't Provide The Username Parameter / HTTP `404`:**
```json
{"error":"You didn't supply an account to get a skin hash from! Add the parameter ?username=IGN_HERE."}
```

Copyright [FaavXD](https://github.com/FaavXD) 2021, all rights reserved.