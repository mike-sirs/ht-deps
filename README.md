# Github safe-settings

This repository helps to create new repositories in Elemental Cognition organization via yaml templates.

## How to add new repository?

To create a new repository via safe-settings you need to add a new YAML file **(extension is mandatory)**. You can use example repo templates for [new repositories](examples/example_new_repo.yml), [importing existing repos](examples/example_import_existing_repo.yaml) or create your own based on [safe-settings examples](https://github.com/github/safe-settings/blob/main-enterprise/docs/sample-settings/repo.yml).

Important notes:

* Your YAML file **must have the same name as your repository**.
* You **must** specify both `force_create` and `auto_init` fields for a new repository.
* Do not forget to add access control via `teams` and `collaborators` - without those sections repository will not be visible for anyone (except admins).
* If you want to use branch protection rules, you need to setup `default_branch` in the `repository` block.
* While we do have linting enabled, PR still can fail after the merge, so please check master branch for errors.
* It is important to verify your repository configuration after creations as some changes might not be applied and do not throw errors.
* Do not skip "required" fields from [safe-settings examples](https://github.com/github/safe-settings/blob/main-enterprise/docs/sample-settings/repo.yml).

While some settings can be applied after repository creation (like teams and branch protection rules), `auto_init` can't be applied retroactively. Ie this setting can be only ommited if you try to add the repo that already exists.
# ht-deps
