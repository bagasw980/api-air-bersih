# Layanan API

- > ## **GET** /layanan

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
          "id_layanan": "1",
          "nama_layanan": "Air Bersih 1",
          "tarif": "4000"
        },
        {
          "id_layanan": "2",
          "nama_layanan": "Air Bersih 2",
          "tarif": "4000"
        },
        {
          "id_layanan": "3",
          "nama_layanan": "Air Bersih 3",
          "tarif": "4000"
        }
      ]
    }
    ```

  - Response Body Failed:

    ```json
    {
      "success": false,
      "message": "Failed to retrieve layanan"
    }
    ```

- > ## **POST** /layanan

  - Headers :

    - Authorization : token

  - Request Body :

    ```json
    { "nama_layanan": "Air Bersih 1", "tarif": "4000" }
    ```

  - Response Body Success 201 :

    ```json
    {
      "success": true,
      "message": "Layanan success created",
      "data": {
        "id_layanan": "1",
        "nama_layanan": "Air Bersih 1",
        "tarif": "4000"
      }
    }
    ```

  - Response Body Failed 400 :

    ```json
    {
      "success": false,
      "message": "Invalid request data"
    }
    ```

- > ## **PUT** /layanan

  - Headers :

    - Authorization : token

  - Request Body :

    ```json
    {
      "id_layanan": "1",
      "nama_layanan": "Air Bersih 1",
      "tarif": "4000"
    }
    ```

  - Response Body Success 201 :

    ```json
    {
      "success": true,
      "message": "Layanan success updated",
      "data": {
        "id_layanan": "1",
        "nama_layanan": "Air Bersih 1",
        "tarif": "4000"
      }
    }
    ```

  - Response Body Failed 400 :

    ```json
    {
      "success": false,
      "message": "Invalid request data"
    }
    ```

- > ## **DELETE** /layanan?id={id}

  - Headers :

    - Authorization : token

  - Request Body : -

  - Response Body Success 201 :

    ```json
    {
      "success": true,
      "message": "Layanan success deleted"
    }
    ```

  - Response Body Failed 400 :

    ```json
    {
      "success": false,
      "message": "Invalid request data"
    }
    ```
