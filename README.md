
<!-- TOC --><a name="a-template-for-your-online-documentation"></a>
# A template for your online documentation

This repository is a template to get you started with building an online documentation.

You see how this documentation is rendered online here: https://euroargodev.github.io/online_documentation

The documentation is built using [Jupyter book](https://jupyterbook.org/en/stable/intro.html) and is hosted/deployed on Github Pages.

<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->

* [Usage](#usage)
  + [Create your own repository](#create-your-own-repository)
  + [Enable doc online rendering](#enable-doc-online-rendering)
  + [Update doc configuration parameters](#update-doc-configuration-parameters)
* [☘ Use Green-Coding energy/CO2e measurements](#-use-green-coding-energyco2e-measurements)
  + [Add your documentation IDs in repository secrets](#add-your-documentation-ids-in-repository-secrets)
     - [Identify your project (repository)](#identify-your-project-repository)
     - [Identify your runs](#identify-your-runs)
  + [Edit the `content/_config.yml` ](#edit-the-content_configyml)

<!-- TOC end -->

<!-- TOC --><a name="usage"></a>
## Usage

You can use this check list to keep track of the procedure. All steps are explained in details below.

- [ ] Create your own repository using this template
- [ ] Enable documentation online rendering (Github Pages)
- [ ] Update documentation content configuration with your own repository data


<!-- TOC --><a name="create-your-own-repository"></a>
### Create your own repository

To create your own documentation using this template, you have to clone this repository using the [green button "Use this template" above](https://github.com/new?template_name=online_documentation&template_owner=euroargodev).

More details here:
https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template


<!-- TOC --><a name="enable-doc-online-rendering"></a>
### Enable doc online rendering

In the repository you created using this template, go to "Settings", then "Pages" and change the "Source" parameter to "Github Actions".


<!-- TOC --><a name="update-doc-configuration-parameters"></a>
### Update doc configuration parameters

Edit the `content/_config.yml` file to update parameters with the new repository data.

2 parameters must be updated:

- replace any template ``euroargodev`` occurrences with your own `OWNER` name,
- replace any template ``online_documentation`` occurences with your `<REPO>` name.

```yml
repository:
  url: https://github.com/<OWNER>/<REPO>

  extra_footer: |
    <div> ️
      <a href="https://github.com/<OWNER>/<REPO>/issues/new?labels=doc-edit&template=doc_edit_template.md" target="_blank">✏ Click here to make a suggestion about this page</a>
      | <a href="https://github.com/<OWNER>/<REPO>/issues/new?labels=doc-error&template=doc_error_template.md" target="_blank">🚨 Report an error on this page</a>
    </div>
    <hr>
    <p>  By the Euro-Argo Dev community using
      <a href="https://jupyterbook.org/intro.html" target="_blank">Jupyter Book</a>.
      
      This work is licensed under a 
      <a href="https://creativecommons.org/licenses/by/4.0/" target="_blank"> Creative Commons Attribution 4.0 Generic License.</a> 
    
    <div>
      <a href="https://metrics.green-coding.io/ci.html?repo=<OWNER>%2F<REPO>&amp;branch=main&amp;workflow=<WORKFLOW_ID>"><img src="https://api.green-coding.io/v1/ci/badge/get?repo=<OWNER>/<REPO>&amp;branch=main&amp;workflow=<WORKFLOW_ID>"></a>   
    </div>
    </p>
```



<!-- TOC --><a name="-use-green-coding-energyco2e-measurements"></a>
## ☘ Use Green-Coding energy/CO2e measurements

Interested in monitoring the energy consumption and CO2e emission associated with the building and deployment of your documentation ?

The documentation template is equiped to do this, but some parameters must be updated first. Follow these steps:

<!-- TOC --><a name="add-your-documentation-ids-in-repository-secrets"></a>
### Add your documentation IDs in repository secrets

In order to identify your documentation within the [📊 euroargodev overall energy & CO2e metrics](https://metrics.green-coding.io/carbondb-lists.html?company_uuid=4f42f511-4d8d-4d30-9c5e-8490f2c68811), you need to create specific IDs for your project and the Github Action machines.

<!-- TOC --><a name="identify-your-project-repository"></a>
#### Identify your project (repository)
1. Get a unique ID from https://www.uuidgenerator.net. Copy the generated ID (it should be a string looking like this example: `4374ec28-7bca-4893-9c69-13e638cda063`)
1. On your repository, go to "Settings", then "Secrets and Variables" and click on the green button "New repository secret"
1. Name it `CARBONDB_PROJECT_UUID` and paste the ID you generated in the previous step in the *secret* field, finalize by clicking on the "Add secret" green button.

<!-- TOC --><a name="identify-your-runs"></a>
#### Identify your runs
1. Get a unique ID from https://www.uuidgenerator.net. Copy the generated ID (it should be a string looking like this example: `4374ec28-7bca-4893-9c69-13e638cda063`)
1. On your repository, go to "Settings", then "Secrets and Variables" and click on the green button "New repository secret"
1. Name it `CARBONDB_MACHINE_UUID_DOC` and paste the ID you generated in the previous step in the *secret* field, finalize by clicking on the "Add secret" green button.

<!-- TOC --><a name="edit-the-content_configyml"></a>
### Edit the `content/_config.yml` 

Once you created you secrets, build the documentation manually by executing the Github action:

<img width="1369" alt="Screenshot 2024-07-02 at 10 38 12" src="https://github.com/euroargodev/online_documentation/assets/1956032/816c4a91-c5dc-4464-a3ed-53ff55ac07c1">

Once the documentation is built and deployed, look at the action summary and look for the workflow parameter in the url:

<img width="1353" alt="Screenshot 2024-07-02 at 10 39 49" src="https://github.com/euroargodev/online_documentation/assets/1956032/f706ccef-4068-48a4-9a94-c653adfd3126">

This workflow id must be used in the repository `content/_config.yml` file: replace any template `104534311` occurences with your own `<WORKFLOW_ID>` value:

```yml
    <div>
      <a href="https://metrics.green-coding.io/ci.html?repo=<OWNER>%2F<REPO>&amp;branch=main&amp;workflow=<WORKFLOW_ID>"><img src="https://api.green-coding.io/v1/ci/badge/get?repo=<OWNER>/<REPO>&amp;branch=main&amp;workflow=<WORKFLOW_ID>"></a>   
    </div>
    </p>
```
