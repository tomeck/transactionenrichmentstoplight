# GitHub Tenant Implementation

*NB: This document was composed in Stoplight using its Markdown editor.  The purpose of the doc is to guide the creation of a Fiserv Dev Portal tenant using only Stoplight and GitHub*

*NB2: The use of Stoplight here is for example purposes.  The same net result can be achieved with any Markdown (or text) editor (e.g. VS Code, Atom, Sublime, vi) and a GitHub repo.*

## GitHub Structure ##

The key to the GitHub Tenant Implementation is the GitHub repo, specifically its folder structure and the location/format of certain key files, as follows:

Type | Name | Purpose
---------|----------|----------
 **file** | tenant_config.yaml | complete configuration of the tenant
 **folder** | docs | all client (developer)-facing documentation
 **folder** | models | all OpenAPI spec's

Note that the GitHub approach described herein obviates the need to implement and support a Tenant Provider API (covered in a separate document)


## Guide to creating a tenant using Stoplight
1. Create a Github repository that will be accessible to the Fiserv Dev Portal platform
*Currently the GitHub repo must be made Public.  We are investigating how to allow Private repo's as well*
1. Use Stoplight to design your API.  It should automatically be stored in the **models** folder
1. Use Stoplight to compose your documents.  Note that Stoplight only supports the creation of Markdown documents, so that's what you will be creating.  Make sure to store those documents in the "docs" folder that is automatically created by Stoplight
1. Create the *tenant_config.yaml* file.  This is the first file that the Fiserv Dev Platform will request and it provides location and other information regarding the docs and models exposed by this tenant

## Publishing your content from Stoplight
This is the easiest part of all of it.  Simply connect an empty GitHub repo with your Stoplight project.  Within Stoplight, just 'push' the site/content to git.   Boom you are done

What happens when you add or change a document, or want to update your Tenant Config file?  Simply make your edits in Stoplight and push them to Git.   Boom - your changes will be instantly active




