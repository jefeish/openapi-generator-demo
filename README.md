![Static Badge](https://img.shields.io/badge/openapi_generator_cli-v7.9.0-blue) ![Static Badge](https://img.shields.io/badge/openapi-v3.0.1-purple)  ![Static Badge](https://img.shields.io/badge/openjdk-v1.8-darkgreen)  ![Static Badge](https://img.shields.io/badge/Maven-v4.0.0-darkred) 

# Openapi-Generator Demo

<img width="200px" src="/docs/images/github-logo.svg"> &nbsp;&nbsp; <img width="45px" src="/docs/images/plus.svg"> &nbsp;&nbsp; <img width="200px" src="/docs/images/openapi-logo.svg">

A simple demonstration of the OpenAPI Generator, demonstrating how to generate code from an OpenAPI specification.

## Introduction

This project demonstrates the use of OpenAPI Generator to generate code from an OpenAPI specification (Yaml). It is intended to provide a straightforward example of how to set up and use the OpenAPI Generator in your own projects.

## OpenAPI-Generator Features

- Generate server stubs and client SDKs from OpenAPI 3.0.1 specifications.
- Supports multiple languages and frameworks. (here we focus on Java)
- Customizable templates for code generation.

## Setup

To set up this project locally, follow these steps:

1. Clone the repository:
  
    ```bash
    git clone https://github.com/jefeish/openapi-generator-demo.git
    cd openapi-generator-demo
    ```

2. Install dependencies:
    Ensure you have Java 1.8, Maven 4.0.0, and OpenAPI Generator CLI 7.9.0 installed.
  
    **Usage**
    
    To generate code from the OpenAPI specification, use the following command:

    - Generate the Code - **Interfaces + Controllers**

    ```bash
    openapi-generator generate -i ./openapi.yml -g spring -o ./ --additional-properties=apiPackage=com.example.demo.api
    ```

   - Generate the Code - **Interfaces ONLY !**

    ```bash
    openapi-generator generate -i ./openapi.yml -g spring -o ./ --additional-properties=apiPackage=com.example.demo.api,interfaceOnly=true
    ```
    
    | Parameter                                   | Description                                                                                      |
    |---------------------------------------------|--------------------------------------------------------------------------------------------------|
    | `-i ./openapi.yml`                          | Specifies the input OpenAPI specification file (YAML or JSON) that defines the API structure.   |
    | `-g spring`                                 | Indicates the generator to use. In this case, it specifies the Spring framework as the target.   |
    | `-o ./`                                     | Sets the output directory where the generated code will be placed. Here, it uses the current directory. |
    | `--additional-properties`                   | Allows you to pass additional properties to customize the code generation process.               |
    | `apiPackage=com.example.demo.api`           | Defines the base package name for the generated API interfaces and implementations.               |
    | `interfaceOnly=true`                        | Instructs the generator to create interfaces only, without implementing controllers. |


### Why We Don’t Generate Controllers:
We want to delegate API endpoint requests to custom controllers, allowing for tailored implementations rather than relying on automatically generated code.
Any changes you make to generated code will be lost when you regenerate the API code. Creating our own controllers prevents the **Openapi-Generator** from overwriting our controller implementations, we use the generated interfaces only as a starting point.
Controllers are where you implement the actual logic for your API endpoints. Developers determine how each API endpoint connects to its controller, this keeps business logic separate from the automatically generated code.


    
 Replace <generator> with the desired generator (e.g., java, python, etc.) and path/to/your/openapi.yaml with the path to your OpenAPI specification file.

    
## Contributing

Contributions are welcome! Please read the contributing guidelines for more information.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
