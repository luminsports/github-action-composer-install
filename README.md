<!-- start title -->

# GitHub Action: composer-install-action

<!-- end title -->

<!-- start description -->

Install Composer Dependencies via Github Action.

<!-- end description -->

<!-- start usage -->

```yaml
- uses: luminsports/github-action-composer@main
  with:
    # Disables installation of require-dev packages.
    no-dev: ""

    # Optimize autoloader during autoloader dump.
    # Default: true
    optimize-autoloader: ""

    # Optimize autoloader during autoloader dump.
    no-autoloader: ""

    # Forces installation from package dist (default behavior).
    # Default: true
    prefer-dist: ""

    # Forces installation from package sources when possible, including VCS
    # information.
    prefer-source: ""

    # Whether to use cache.
    # Default: true
    cache: ""

    # Whether to create artifacts.
    # Default: true
    artifact: ""

    # Name of generated artifact.
    # Default: composer
    artifact-name: ""

    # Name of generated artifact.
    # Default: vendor.tar
    artifact-path: ""

    # Number of days that the artifact should be retained for.
    # Default: 7
    artifact-retention-days: ""
```

<!-- end usage -->

<!-- start inputs -->

| **Input**                     | **Description**                                                                    | **Default**  | **Required** |
| :---------------------------- | :--------------------------------------------------------------------------------- | :----------: | :----------: |
| **`no-dev`**                  | Disables installation of require-dev packages.                                     |              |  **false**   |
| **`optimize-autoloader`**     | Optimize autoloader during autoloader dump.                                        |    `true`    |  **false**   |
| **`no-autoloader`**           | Optimize autoloader during autoloader dump.                                        |              |  **false**   |
| **`prefer-dist`**             | Forces installation from package dist (default behavior).                          |    `true`    |  **false**   |
| **`prefer-source`**           | Forces installation from package sources when possible, including VCS information. |              |  **false**   |
| **`cache`**                   | Whether to use cache.                                                              |    `true`    |  **false**   |
| **`artifact`**                | Whether to create artifacts.                                                       |    `true`    |  **false**   |
| **`artifact-name`**           | Name of generated artifact.                                                        |  `composer`  |  **false**   |
| **`artifact-path`**           | Name of generated artifact.                                                        | `vendor.tar` |  **false**   |
| **`artifact-retention-days`** | Number of days that the artifact should be retained for.                           |     `7`      |  **false**   |

<!-- end inputs -->

<!-- start outputs -->

| **Output**               | **Description**                                                                       | **Default** | **Required** |
| :----------------------- | :------------------------------------------------------------------------------------ | ----------- | ------------ |
| `checkstyle-result`      | Checkstyle report generate by php-cs-fixer                                            |             |              |
| `pull-request-number`    | The pull request number                                                               |             |              |
| `pull-request-url`       | The URL of the pull request.                                                          |             |              |
| `pull-request-operation` | The pull request operation performed by the action, `created`, `updated` or `closed`. |             |              |
| `pull-request-head-sha`  | The commit SHA of the pull request branch.                                            |             |              |

<!-- end outputs -->
