# Git Repository with Only Submodules

This repository is structured to include only submodules. Follow the steps below to initialize and update the submodules.

## Initializing Submodules

To clone the repository and initialize the submodules, use the following commands:

```sh
git clone --recurse-submodules <repository_url>
```

If you have already cloned the repository, you can initialize and update the submodules with:

```sh
git submodule update --init --recursive
```

## Updating Submodules

To update the submodules to the latest commit, use:

```sh
git submodule update --remote --merge
```

## Adding a New Submodule

To add a new submodule to the repository, use:

```sh
git submodule add <submodule_repository_url> <path_to_submodule>
git commit -m "Add new submodule"
```

## Removing a Submodule

To remove a submodule, follow these steps:

1. Delete the relevant section from the `.gitmodules` file.
2. Remove the submodule entry from `.git/config`.
3. Run `git rm --cached <path_to_submodule>`.
4. Delete the submodule directory from the working tree.

```sh
git rm --cached <path_to_submodule>
rm -rf <path_to_submodule>
git commit -m "Remove submodule"
```

## Common Commands

- **List all submodules**: `git submodule`
- **Status of submodules**: `git submodule status`
- **Sync submodules**: `git submodule sync`

For more information, refer to the [Git Submodules Documentation](https://git-scm.com/book/en/v2/Git-Tools-Submodules).
