# A template for your online documentation

This repository is a template to get you started with building an online documentation.

Checkout how this documentation is rendered online here: https://euroargodev.github.io/online_documentation

The documentation is built using the [Jupyter book](https://jupyterbook.org/en/stable/intro.html) and hosted/deployed on Github Pages.

## Usage

### Create your own repository

To create your own documentation using this template, you have to clone this repository using the [green button "Use this template" above](https://github.com/new?template_name=online_documentation&template_owner=euroargodev).

More details here:
https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template

- [ ] Create your own repository

### Enable documentation online rendering

In the repository you created using this template, go to "Settings", then "Pages" and change the "Source" parameter to "Github Actions".

- [ ] Github Pages enabled

### Update configuration with new repo

Edit the `content/_config.yml` and update parameters with the new repo data.

2 parameters must be updated:

- replace any template `euroargodev` occurrences with your own `OWNER` name,
- replace any template `online_documentation` occurences with your `<REPO>` name.

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

- [ ] Content configuration updated with my own repository data


## Use Green-Coding energy/CO2e measurements

Interesting in monitoring the energy consumption and CO2e emission associated with the building and deployment of your documentation ?

The documentation template is equiped to do this, but some parameters msut be updated first. Follow these steps:

### Edit the `content/_config.yml` 

and update parameters with the new repo data.

1 parameter must be updated:

- replace any template `104534311` occurences with your `<WORKFLOW_ID>` value.


