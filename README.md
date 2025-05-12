# checks-packages-create
A Liquibase flow file to create themed checks packages, and the overall checks-package file to be used in checks commands.

## This repo is primarily about the file `liquibase-create-checks-packages.flow.yaml`
This flow file generates the checks-packages artifacts shipped with Liquibase:
* liquibase.checks-settings.conf (if it doesnt exist)
* liquibase.checks-package.yaml
* checks-packages (a directory)

  -- liquibase.checks.access-control.yaml

  -- liquibase.checks.data-protection.yaml

  -- liquibase.checks.schema-protection.yaml 

  -- liquibase.checks.changeset-standards.yaml

  -- liquibase.checks.coding-standards.yaml
 
But the real value is to serve as a template for generating your own checks packages
if you already have a base checks-settings file which you would like to split into 
themed checks settings file in a sub-dir, controlled by a checks-package file.




## quick start

1. download `liquibase.create-check-package.flow.yaml` and `liquibase.checks-package-header.yaml`
2. place in CWD
3. run `liquibase flow --checks-settings-file=liquibase.create-check-package.flow.yaml`
4. this will create sub-dir (`./checks-pkgs`) with 5 themed checks-settings files
5. this will create a `liquibase.checks-package.yaml` which lists these packages


## about the files

### `liquibase.checks-package-header.yaml`
The contents of this file are injected/prepended to the `liquibase.checks-package.yaml` created by the flow file.
The contents are useful information about checks package files, with links to docs to learn more.
