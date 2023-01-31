[OpenAPI](https://www.openapis.org/) is a specification for describing a REST API. You can think of the OpenAPI specification as a DITA specification. DITA has specific XML elements that are used to define help components and the required order and hierarchy for those elements. Various tools can read DITA and build a documentation website based on the information.

In OpenAPI, instead of XML, there is a set of JSON objects with a specific schema that defines their name, order, and content. This JSON file (often expressed in YAML instead of JSON) describes each part of the API. By describing the API in a standard format, publishing tools can parse the API information programmatically and display each component in a stylized, interactive way.

# A look at the OpenAPI specification

The official description of the OpenAPI specification is available in [the Github repository](https://github.com/OAI/OpenAPI-Specification). The OpenAPI elements are `paths`, `parameters`, `responses`, and `security`. Each of these elements is a JSON object that contains properties and arrays.

In the OpenAPI specification, your endpoints are `paths`. The endpoint `/pet`, in the OpenAPI specification, might look like this:

```
paths:
    /pets:
        get:
            summary: List all pets
            operationId: listPets
            tags:
                - pets
            parameters:
                - name: limit
                in: query
                description: How many items to return at one time (max 100)
                required: false
                schema:
                    type: integer
                    format: int32
            responses:
                '200':
                description: An paged array of pets
                headers:
                    x-next:
                        description: A link to the next page of responses
                        schema:
                            type: string
                content:
                    application/json:
                        schema:
                            $ref: "#/components/schemas/Pets"
            default:
                description: unexpected error
                content:
                    application/json:
                        schema:
                            $ref: "#/components/schemas/Error"

```

This is YAML format, taken from [Swagger PetStore](http://petstore.swagger.io/)

Here is what the objects mean in this code:

-   `/pets`- endpoint of path;
-   `get`- HTTP method;
-   `parameters`- list of endpoint parameters;
-   `responses`- list of responses to the request
-   `200`- HTTP status code
-   `$ref`is a reference to another part of the implementation where the response is defined (in `components`). OpenAPI has many `$ref`links like this to keep the code clean and easy to reuse.

> **Note:** The OpenAPI specification is general enough to describe almost every REST API, so some parts may be more applicable than others.

# Specification check

When creating an OpenAPI specification, instead of working in a text editor, you can write your code in [the Swagger editor](http://editor.swagger.io/). The Swagger editor dynamically checks the content to determine if the generated spec is valid.

If you make a mistake while writing code in the Swagger editor, you can quickly fix it before you continue, instead of waiting for the build to run and fix the errors.

For the specification format, we have the choice of JSON or YAML operation. The code example above is in [YAML](https://yaml.org/). YAML has an official definition: "YAML is not a markup language", which means that YAML does not have markup tags `<>`like other markup languages ​​such as XML do.

YAML relies on spaces and colons to establish object syntax. This space-sensitive formatting makes the code more human-readable. However, sometimes there may be difficulties with the placement of the correct intervals.

# Automatic generation of OpenAPI file from code annotations

Instead of manually encoding the document in the OpenAPI specification, you can also automatically generate it from annotations in the code. This developer-centric approach makes sense if there are a large number of APIs, or if it's impractical for technical writers to create this documentation.

Swagger provides many libraries that you can add to your code to create a document in a BOM. These Swagger libraries parse annotations that developers add and generate a document in the OpenAPI specification. These libraries are considered part of the [Swagger Codegen](https://swagger.io/tools/swagger-codegen/) project. Annotation methods differ depending on the programming language. For example, here is [a code annotation guide with Swagger for Scalatra](https://www.infoq.com/articles/swagger-scalatra). For more information on Codegen, see [Comparing Swagger API Auto Code Generation Tools](https://apievangelist.com/2015/06/06/comparison-of-automatic-api-code-generation-tools-for-swagger/) by Evangelist API. For additional tools and libraries, see [Swagger Integrations and Tools](https://swagger.io/tools/open-source/open-source-integrations/) and["Open Source Integration"](https://swagger.io/tools/open-source/open-source-integrations/).

While this approach "automates" specification generation, you still need to understand what annotations to add and how to add them (this process is not too different from Javadoc comments and annotations). Next, you need to write content for each of the annotation values ​​(describing the endpoint, parameters, etc.).

In short, everything needs work - the automated part causes the Codegen libraries to generate model definitions and a valid document that conforms to the OpenAPI schema. However, many developers prefer this approach because it offers a way to generate documentation from code annotations, which developers have been doing for years with other programming languages ​​such as Java (using [Javadoc](https://www.oracle.com/technetwork/articles/java/index-137868.html)) or C++ (using [Doxygen](http://www.doxygen.nl/) ). Generating documentation from code results in less documentation rejection. Documents will remain relevant if closely linked to the code.
