# Pelanggan API

- > ## **GET** /pelanggan

  - Headers :

    - Authorization : token

  - Request Body : -

  - Response Body Success :

    ```json
    {
      "status": "200",
      "message": "success",
      "data": [
        {
          "id_pelanggan": "PL-10023",
          "nama_pelanggan": "Budiyanto",
          "alamat": "Sukoharjo",
          "no_telepon": "6282220542202"
        },
        {
          "id_pelanggan": "PL-10023",
          "nama_pelanggan": "Budiyanto",
          "alamat": "Sukoharjo",
          "no_telepon": "6282220542202"
        },
        {
          "id_pelanggan": "PL-10023",
          "nama_pelanggan": "Budiyanto",
          "alamat": "Sukoharjo",
          "no_telepon": "6282220542202"
        }
      ]
    }
    ```

  - Response Body Failed:

    ```json
    {
      "status": "500",
      "message": "Server error"
    }
    ```

- > ## **GET** /pelanggan/{id}

  - Headers :

    - Authorization : token

  - Request Body : -

  - Response Body Success :

    ```json
    {
      "status": "200",
      "message": "success",
      "data": {
        "id_pelanggan": "PL-10023",
        "nama_pelanggan": "Budiyanto",
        "alamat": "Sukoharjo",
        "no_telepon": "6282220542202"
      }
    }
    ```

  - Response Body Failed:

    ```json
    {
      "status": "500",
      "message": "Server error"
    }
    ```
