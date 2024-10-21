# checks-packages-create
Liquibase flow file to create themed checks packages files 

Usage steps to come...

quick summary:
1. download `liquibase.create-check-package.flow.yaml` and `liquibase.checks-package-header.yaml`
2. place in CWD
3. run `liquibase flow --checks-settings-file=liquibase.create-check-package.flow.yaml`
4. this will create sub-dir (`./checks-pkgs`) with 5 themed checks-settings files
5. this will create a `liquibase.checks-package.yaml` which lists these packages
