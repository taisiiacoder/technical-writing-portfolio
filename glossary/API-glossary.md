# A

### API

Application Programming Interface. Allows different systems to communicate with each other programmatically. The two types of API are REST API (Web API) and Native Library API.

### API console

Interactive display for RAML specification. Similar to Swagger UI but for RAML.

### Apimatic

Supports most REST API description formats (OpenAPI, RAML, API Blueprint) and provides SDK code generation, conversions from one specification format to another, and many other services. APIMATIC "lets you define APIs and generate SDKs for over 10 languages." For example, you can automatically convert Swagger 2.0 to 3.0 using [the Transformer API](https://www.apimatic.io/transformer) service on this site. CM. <https://apimatic.io/> and their [documentation](https://docs.apimatic.io/).

### API Transformer

A cross-platform service provided by APIMATIC that automatically converts your BOM document from one format or version to another. See [apimatic.io/transformer](https://www.apimatic.io/transformer).

### Apiary

A platform that supports the full lifecycle of API design, development, and deployment. For interactive documentation, Apiary supports the Blueprint API specification is similar to OpenAPI or RAML but contains more Markdown elements. It also now supports the OpenAPI specification. See [apiary.io](https://apiary.io/).

### API Blueprint

The Blueprint API specification is an alternative to the OpenAPI or RAML specification. The Blueprint API uses Markdown syntax. See [Blueprint API](https://apiblueprint.org/).

### Apigee

Similar to Apiary, Apigee provides services for managing the entire API life cycle. Specifically, Apigee enables "to manage API complexity and risk in a multi-cloud and hybrid cloud world by providing security, visibility, and performance across the entire API environment." It supports the OpenAPI specification. See [apigee.com](https://apigee.com/api-management/).

### Asciidoc

Asciidoc is a lightweight text format that provides more semantic features than Markdown. Used in some static site generators like [Asciidoctor](https://asciidoctor.org/) or [Nanoc](https://nanoc.ws/). See [asciidoc.org](http://asciidoc.org/).

# B

### branch

In Git, a branch is a copy of a repository that is often used to develop new features. Usually you work in branches and then merge your branch into the main branch. See [git-branch](https://git-scm.com/docs/git-branch).

# C

### clone

Clone is the command user calls to copy a repository. The first step in working with any repository is to clone the repo locally. Git is a distributed version control system, so everyone who works on it has a local copy (clone) on their machines. The central repository is called the source. Each user can pull updates from the source and push updates to the source. See [git-clone](https://git-scm.com/docs/git-clone).

### commit

Commit is a snapshot of your changes in a repo. Git saves the commit as a snapshot in time that you can revisit later if needed. You commit your changes before pulling from the origin, or before merging your branch with another branch. See [git commit](https://git-scm.com/docs/git-commit).

### CRUD

CRUD is the abbreviation for Create, Read, Update, Delete. These four programming operations are often compared to POST, GET, PUT, and DELETE in REST APIs.

### curl

Curl is a command line utility that allows you to make HTTP requests with various options and methods. The command line can be used instead of navigating to web resources in the browser's address bar to get the same resources retrieved as text.

# E

### endpoints and methods

Endpoints show how to reach the resource, while methods indicate the allowed actions (GET, POST, DELETE, and others) with the resource.

The same resource can have multiple associated endpoints, each with different paths, methods, and returning different information about the same resource. Endpoints can have a short description similar to a resource description. Also, the endpoint only shows the end path of the resource's URL, without the base path common to all endpoints.

# G

### GitLab

Code repository management platform used by company developers.

### git repo

The git repository stores the project code. Only non-binary (human-readable) text files are kept in the repository because Git can run diff on text files and show changes.

### gulp

[Gulp](https://gulpjs.com/) is a web application build tool that automates repetitive tasks like building and minifying CSS and JS files, running tests, reloading the browser, and more. Thus, Gulp speeds up and optimizes the web development process. In this article, we will cover the basics of using this tool.

# H

### HAT

Help Authoring Tool. Refers to traditional help authoring tools (RoboHelp, Flare, Author-it) and is used by technical writers for documentation. API documentation tools tend to use docs-as-code tools instead of HAT.

### HATEOS

Abbreviation for Hypermedia as the Engine of Application State. Hypermedia is one of the characteristics of REST that is often overlooked or missing from REST APIs. In API responses, responses that span multiple pages should provide users with links to other items.

### Header parameters

Parameters that are included in the request header. Usually authorization parameters are passed in the header.

# J

### JSON

JavaScript Object Notation. A lightweight syntax containing objects and arrays, commonly used (instead of XML) to return information from a REST API. <http://www.json.org/>

# M

### method

Permitted resource operation: GET, POST, PUT, DELETE. These operations determine whether you are reading information, creating new information, updating existing information, or deleting information.

# O

### OAS

Abbreviation of OpenAPI Specification

### OpenAPI

The official name for the OpenAPI specification. The OpenAPI specification provides a set of properties that can be used to describe a REST API. When a specification is valid, it can be used to create interactive documentation, build client SDKs, run unit tests, and more. Specification details on [GitHub](https://github.com/OAI/OpenAPI-Specification). As part of the Open API initiative with the Linux Foundation, the OpenAPI specification aims to be vendor independent.

### open API contract

Synonymous with "OpenAPI Specification"

### OpenAPI specification

A YAML or JSON file describing the REST API. Follows the format of the OpenAPI specification. [openapis.org](https://www.openapis.org/)

# P

### Parameters

Parameters are data that can be passed to an endpoint (such as specifying a response format or a return amount) to influence the response. There are four types of parameters: header parameters, path parameters, query string parameters, and request body parameters.

Different types of parameters are often documented in separate groups on the same page. Not all endpoints can contain all parameter types.

### Path parameters

Parameters that appear in the endpoint path, before the query string. Path parameters are usually set in curly braces.

### pull

Data extraction. In Git, when you pull data from the origin (the main place where you cloned the repo), you get the latest updates to the local system. On startup git pull, Git saves updates from the source to a local copy. If the merge cannot happen automatically, merge conflicts will be displayed. [Git-pull](https://git-scm.com/docs/git-pull).

### pull request

A request from an external contributor to merge the cloned branch back into the master branch. The pull request workflow is used in projects because developers outside the team usually don't have contributor permissions to merge updates into the repository. Gitlab provides a convenient interface for creating and processing such requests. [pull request](https://git-scm.com/docs/git-request-pull)

### push

Submit changes. The command in Git to push changes to the latest update source from the local copy (git push). The updates sync the local copy with the remote repo. [git push](https://git-scm.com/docs/git-push).

# Q

### Query string parameters

Options that appear at the end point after the sign.

# R

### repos

A tool to consolidate and manage many small repos with one system. [git repo](https://code.google.com/archive/p/git-repo/).

### request

Inquiry. A way to get the information returned by the API. In the request, the client provides a resource URL with the appropriate authorization to the API server. The API returns a response with the requested information.

### request body parameters

Parameters in the request body (in JSON format).

### response

Information returned by the API after a user makes the request. Responses are usually in JSON or XML format.

### response example and schema

Response example shows an example of a response from an example request. The response schema defines all possible elements in the response. The sample response is not exhaustive for all parameter configurations or operations, but it must match the parameters passed in the sample request. The response lets developers know if the resource contains the information they want, the format, and how that information is structured and tagged.

The response description is the response schema. The response schema documents the response in a more complete, general way, listing each returned property, what each property contains, the value data format, structure, and other details.

### resource description

"Resources" refers to the information returned by the API. Most APIs have different categories of information or different resources that can be returned.

The description of the resource is short (1-3 sentences) and usually begins with a verb. Resources typically have different endpoints for accessing the resource and multiple methods for each endpoint. The individual resource page usually describes the shared resource as well as the set of endpoints for accessing the resource.

### REST API

Abbreviation for Representational State Transfer. REST API uses web protocols (HTTP) to send requests and provide responses regardless of language. Users can choose any programming language they want to make when making calls.

# S

### SDK

Software development kit - Software development kit. Developers often create SDKs to accompany REST APIs. An SDK helps developers implement APIs using a specific language, such as Java or PHP.

### Swagger

Swagger is one of the API tools associated with the OpenAPI specification. Some of these tools include [Swagger Editor](https://swagger.io/tools/swagger-editor/), [Swagger UI](https://swagger.io/tools/swagger-ui/), [Swagger Codegen](https://swagger.io/tools/swagger-codegen/), [SwaggerHub](https://app.swaggerhub.com/home) and [more](https://swagger.io/tools/). These tools are managed by [Smartbear](https://smartbear.com/). More information: [Swagger Tools](https://swagger.io/tools/). "Swagger" was the original name of the OpenAPI specification, but the name was later changed to [OpenAPI](https://github.com/OAI/OpenAPI-Specification/) to reinforce the open, non-proprietary nature of the standard.

### Swagger Codegen

Generates client SDK code for many different languages ​​(such as Java, JavaScript, Scala, Python, PHP, Ruby, Scala, and more). The client SDK code helps developers integrate platform-specific APIs and provides more robust implementations that can include scaling, multithreading, and other required code. Swagger Codegen generates client SDKs in almost every programming language. More information at [Swagger Codegen](https://swagger.io/tools/swagger-codegen/).

### swagger editor

An online editor that checks the OpenAPI documentation against the rules of the OpenAPI specification. The Swagger editor flags errors and provides formatting advice. [swagger editor](https://swagger.io/tools/swagger-editor/)

### SwaggerUI

An open source web framework that parses the OpenAPI specification and generates an interactive documentation website page. Swagger UI is a tool that transforms a specification into [a Petstore-like site](http://petstore.swagger.io/).

### swaggerhub

A site developed by Smartbear to help teams collaborate on the OpenAPI specification. In addition to creating online documentation from SwaggerHub, you can create many client and server SDKs and other services.

# V

### VCS

Abbreviation for version control system. Git and Mercurial example

### Version control system

A code management system based on commits that keeps content in certain states. It allows you to return to previous states, split the code into different versions, branches, etc.

# Y

### YAML

Recursive abbreviation for "YAML Ain't No Markup Language". Human-readable, space-sensitive syntax used in the OpenAPI specification documentation.
