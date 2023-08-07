# Pelanggan API

- > ## **GET** /pelanggan

  - Headers :

    - Authorization : token

  - Request Body : -

  - Response Body Success 200 :

    ```json
    {
      "success": true,
      "message": "success",
      "data": [
        {
          "id_pelanggan": "PL-10023",
          "nama_pelanggan": "Budiyanto",
          "alamat": "Sukoharjo",
          "layanan": "Air Bersih 1",
          "no_telepon": "6282220542202"
        },
        {
          "id_pelanggan": "PL-10023",
          "nama_pelanggan": "Budiyanto",
          "alamat": "Sukoharjo",
          "layanan": "Air Bersih 1",
          "no_telepon": "6282220542202"
        },
        {
          "id_pelanggan": "PL-10023",
          "nama_pelanggan": "Budiyanto",
          "alamat": "Sukoharjo",
          "layanan": "Air Bersih 1",
          "no_telepon": "6282220542202"
        }
      ]
    }
    ```

  - Response Body Failed :

    ```json
    {
      "success": false,
      "message": "Failed to retrieve pelanggan"
    }
    ```

- > ## **GET** /pelanggan/detail?id={id}

  - Headers :

    - Authorization : token

  - Request Body : -

  - Response Body Success 200 :

    ```json
    {
      "success": true,
      "message": "success",
      "data": {
        "id_pelanggan": "PL-10023",
        "nama_pelanggan": "Budiyanto",
        "alamat": "Sukoharjo",
        "layanan": "Air Bersih 1",
        "no_telepon": "6282220542202"
      }
    }
    ```

  - Response Body Failed:

    ```json
    {
      "success": false,
      "message": "Failed to retrieve pelanggan"
    }
    ```

- > ## **POST** /pelanggan

  - Headers :

    - Authorization : token

  - Request Body :

    ```json
    {
      "nama_pelanggan": "Budiyanto",
      "alamat": "Sukoharjo",
      "no_telepon": "6282220542202",
      "layanan": 1
    }
    ```

  - Response Body Success 201 :

    ```json
    {
      "success": "201",
      "message": "Pelanggan success created",
      "data": {
        "id_pelanggan": "PL-10023",
        "nama_pelanggan": "Budiyanto",
        "alamat": "Sukoharjo",
        "no_telepon": "6282220542202",
        "layanan": 1
      }
    }
    ```

  - Response Body Failed 400:

    ```json
    {
      "success": false,
      "message": "Invalid request data"
    }
    ```

- > ## **PUT** /pelanggan

  - Headers :

    - Authorization : token

  - Request Body :

    ```json
    {
      "id_pelanggan": "PL-10023",
      "nama_pelanggan": "Budiyanto",
      "alamat": "Sukoharjo",
      "no_telepon": "6282220542202",
      "layanan": 1
    }
    ```

  - Response Body Success 201 :

    ```json
    {
      "success": "201",
      "message": "Pelanggan success updated",
      "data": {
        "id_pelanggan": "PL-10023",
        "nama_pelanggan": "Budiyanto",
        "alamat": "Sukoharjo",
        "no_telepon": "6282220542202",
        "layanan": 1
      }
    }
    ```

  - Response Body Failed 400:

    ```json
    {
      "success": false,
      "message": "Invalid request data"
    }
    ```

- > ## **DELETE** /pelanggan?id={id}

  - Headers :

    - Authorization : token

  - Request Body : -

  - Response Body Success 201 :

    ```json
    {
      "success": "201",
      "message": "Pelanggan success deleted"
    }
    ```

  - Response Body Failed 400:

    ```json
    {
      "success": false,
      "message": "Invalid request data"
    }
    ```
