# Deploying your science app.

In order to deploy a science app one shoudl use the [Create Science App form at the Araport Portal](https://araport-dev.tacc.utexas.edu/node/add/science-app).

## Application Name
** Required: ** False

If the user fills in this field the value from the application manifest will be overwritten by this value.

If the user **does not** fills in this field the value from the manifest will be used.

## Application repository URL
** Required: ** True

The user must fill in the git repository URL. The repository must be a public repository for the portal to be able to clone it.

## Release version
** Required: ** False

A release version is a snapshot of the specified repository. If no value is given the master branch will be used.

In order to create a **Relase Version**, the user must create a tag pointing to the version of the code the user would like to use.

The steps are listed below.

1. Modify the code of your repository as needed.
2. Push changes to your repository
  2.1 `$ git push origin <branch>`
3. Create tag
  3.1 `$ git tag -a v0.1 -v 'my version 0.1'`
4. Create tag in remote repository
  4.1 `$ git push origin v0.1`

For more information read the [Git documentation on Tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging)

## Application Description
** Required: ** False

If the user fills in this field the value from the application manifest will be overwritten by this value.

If the user **does not** fills in this field the value from the manifest will be used.

## Notes

When listing installed applications by accessing My Apps in (your account)[https://araport-dev.tacc.utexas.edu/user], the user can `hard refresh` an application. 

This is done by editing the application and checking the checkbox with the label `Force Reload` and clicking on the `Save` button. 

This will force the portal to delete every file linked to the application (e.g. code, libraries, assets) and re-clone the repository.

This is usually done if the user suspects there is an issue with the way the repository was cloned or if the application has moved to another repository.
