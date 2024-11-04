# Developer Notes

- Generate the Code - Interfaces + Controllers

    ```bash
    openapi-generator generate -i ./openapi.yml -g spring -o ./ --additional-properties=apiPackage=com.example.demo.api
    ```

- Generate the Code - Interfaces ONLY !

    ```bash
    openapi-generator generate -i ./openapi.yml -g spring -o ./ --additional-properties=apiPackage=com.example.demo.api,interfaceOnly=true
    ```