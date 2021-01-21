# Container Tenant Implementation

*NB: This document was composed in Stoplight using its Markdown editor.  The purpose of the doc is to guide the creation of a Fiserv Dev Portal tenant using only Stoplight and a Docker-style container*

*NB2: The use of Stoplight here is for example purposes.  The same net result can be achieved with any Markdown (or text) editor (e.g. VS Code, Atom, Sublime, vi) and a GitHub repo.*

## Folder Structure ##

The key to the Container Tenant Implementation is the folder structure and the location/format of certain key files, as follows:

Type | Name | Purpose
---------|----------|----------
 **file** | /content/tenant_config.yaml | complete configuration of the tenant
 **folder** | /content/docs | all client (developer)-facing documentation
 **folder** | /content/models | all OpenAPI spec's

Note that the GitHub approach described herein obviates the need to implement and support a Tenant Provider API (covered in a separate document), however you must be able to expose a Route to the /content folder within your container.  This Route is the single entry point that the Fiserv Dev Platform will use to communicate with the Tenant


## Guide to creating a tenant using Stoplight
1. Use Stoplight to design your API.  It should automatically be stored in the **models** folder
1. Use Stoplight to compose your documents.  Note that Stoplight only supports the creation of Markdown documents, so that's what you will be creating.  Make sure to store those documents in the "docs" folder that is automatically created by Stoplight
1. Create the *tenant_config.yaml* file.  This is the first file that the Fiserv Dev Platform will request and it provides location and other information regarding the docs and models exposed by this tenant

## Publishing your content via a Container

