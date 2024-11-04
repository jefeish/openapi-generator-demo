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

    ```bash
    openapi-generator-cli generate -i path/to/your/openapi.yaml -g <generator> -o output_directory
    Replace <generator> with the desired generator (e.g., java, python, etc.) and path/to/your/openapi.yaml with the path to your OpenAPI specification file.
    ```
    
## Contributing

Contributions are welcome! Please read the contributing guidelines for more information.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
