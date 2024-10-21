# checks-packages-create
A Liquibase flow file to create themed checks packages, and the overall checks-package file to be used in checks commands.


## quick start

1. download `liquibase.create-check-package.flow.yaml` and `liquibase.checks-package-header.yaml`
2. place in CWD
3. run `liquibase flow --checks-settings-file=liquibase.create-check-package.flow.yaml`
4. this will create sub-dir (`./checks-pkgs`) with 5 themed checks-settings files
5. this will create a `liquibase.checks-package.yaml` which lists these packages


## about the files

### `liquibase.checks-package-header.yaml`
The contents of this file are injected/prepended to the `liquibase.checks-package.yaml` created by the flow file.
The contents are useful informatiomn about checks package files, with links to docs to learn more.
