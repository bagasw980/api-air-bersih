# Pemakaian API

- > ## **GET** /pemakaian

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
          "id_pemakaian": "1",
          "nama_pelanggan": "Budi",
          "meter_awal": 120,
          "meter_akhir": 150,
          "tarif": 78000,
          "tgl_input": "2023-10-20",
          "inputed_by": 1,
          "paymaster": null,
          "status": "Belum Bayar",
          "tgl_bayar": null,
          "denda": null
        },
        {
          "id_pemakaian": "2",
          "nama_pelanggan": "Santoso",
          "meter_awal": 120,
          "meter_akhir": 150,
          "tarif": 78000,
          "tgl_input": "2023-10-20",
          "inputed_by": 1,
          "paymaster": 2,
          "status": "Sudah Bayar",
          "tgl_bayar": "2023-10-20",
          "denda": null
        },
        {
          "id_pemakaian": "3",
          "nama_pelanggan": "Indri",
          "meter_awal": 120,
          "meter_akhir": 150,
          "tarif": 78000,
          "tgl_input": "2023-10-20",
          "inputed_by": 1,
          "paymaster": 2,
          "status": "Sudah Bayar",
          "tgl_bayar": "2023-10-20",
          "denda": null
        }
      ]
    }
    ```

  - Response Body Failed:

    ```json
    {
      "success": false,
      "message": "Failed to retrieve pemakaian"
    }
    ```

- > ## **GET** /pemakaian?id={id}

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
          "id_pemakaian": "1",
          "nama_pelanggan": "Budi",
          "meter_awal": 120,
          "meter_akhir": 150,
          "tarif": 78000,
          "tgl_input": "2023-10-20",
          "inputed_by": 1,
          "paymaster": 2,
          "status": "Sudah Bayar",
          "tgl_bayar": "2023-10-20",
          "denda": null
        },
        {
          "id_pemakaian": "5",
          "nama_pelanggan": "Budi",
          "meter_awal": 150,
          "meter_akhir": 180,
          "tarif": 78000,
          "tgl_input": "2023-11-20",
          "inputed_by": 1,
          "paymaster": 2,
          "status": "Sudah Bayar",
          "tgl_bayar": "2023-10-20",
          "denda": null
        },
        {
          "id_pemakaian": "10",
          "nama_pelanggan": "Budi",
          "meter_awal": 180,
          "meter_akhir": 210,
          "tarif": 78000,
          "tgl_input": "2023-12-20",
          "inputed_by": 1,
          "paymaster": null,
          "status": "Belum Bayar",
          "tgl_bayar": null,
          "denda": null
        }
      ]
    }
    ```

  - Response Body Failed:

    ```json
    {
      "success": false,
      "message": "Failed to retrieve pemakaian"
    }
    ```

- > ## **GET** /pemakaian/detail?id={id}

  - Headers :

    - Authorization : token

  - Request Body : -

  - Response Body Success 200 :

    ```json
    {
      "success": true,
      "message": "success",
      "data": {
        "id_pemakaian": "1",
        "nama_pelanggan": "Budi",
        "meter_awal": 120,
        "meter_akhir": 150,
        "tarif": 78000,
        "tgl_input": "2023-10-20",
        "inputed_by": 1,
        "paymaster": 2,
        "status": "Sudah Bayar",
        "tgl_bayar": "2023-10-20",
        "denda": null
      }
    }
    ```

  - Response Body Failed:

    ```json
    {
      "success": false,
      "message": "Failed to retrieve pemakaian"
    }
    ```

- > ## **POST** /pemakaian

  - Headers :

    - Authorization : token

  - Request Body :

    ```json
    {
      "id_pelanggan": 1,
      "meter_akhir": 150,
      "tgl_input": "2023-10-20",
      "inputed_by": 1
    }
    ```

  - Response Body Success 201 :

    ```json
    {
      "success": "201",
      "message": "Pemakaian success created"
    }
    ```

  - Response Body Failed 400:

    ```json
    {
      "success": false,
      "message": "Invalid request data"
    }
    ```

- > ## **DELETE** /pemakaian?id={id}

  - Headers :

    - Authorization : token

  - Request Body : -

  - Response Body Success 201 :

    ```json
    {
      "success": "201",
      "message": "Pemakaian success deleted"
    }
    ```

  - Response Body Failed 400:

    ```json
    {
      "success": false,
      "message": "Invalid request data"
    }
    ```
