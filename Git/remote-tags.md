```git branch --all``` lists all branches whether remote or local. However, there is no way to list all remote tags.

```git tag``` or ```git tag -l``` will only list local tags.

In order to bring all the remote tags to local, you need to run the following command:

```git fetch --tags```

After this, ```git tag``` should list all the local tags.
