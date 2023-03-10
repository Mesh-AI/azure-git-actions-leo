# Test: Git actions + Test/Plan/Deploy workflows in a simplified way 

* Do not use this repo! Test only!

## Supporting Resources:

 - rg-terraform-github-actions-leo (.tfvars bearer)

### Workflows:

  * **Terraform Unit Tests**: This workflow runs on every commit and is composed of a set of unit tests on the infrastructure code. The tests aim to ensure the code is properly linted and follows terraform best practices. Additionally, certifies that the code is syntactically correct and internally consistent. Lastly, runs checkov (opensource static code analysis tool for IaC) for security and compliance issues.

  * **Terraform Plan / Apply**: This workflow runs on every pull request and on each commit to the main branch. The plan stage of the workflow is used to understand the impact of the IaC changes on the Azure environment by running terraform plan command.

  * **Terraform Drift Detection**: This workflow runs on a periodic basis to scan your environment for any configuration drift or changes made outside of terraform. If any drift is detected, a GitHub Issue is raised to alert the maintainers of the project.
