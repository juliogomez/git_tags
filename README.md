# Git Tags

When you need to switch among different versions of code in a file, you have the option of using Git tags instead of branches. The main difference is that branches may be changed with a commit, they are mutable, while tagged commits cannot be changed, they are immutable.

Let’s give tags a try…

First create and move into a working directory:

```
mkdir git_tags
cd git_tags
```

Initialize *git* in that directory:

```
git init
```

Now edit a test file called 'version' and write just one line with "FIRST":

```
echo "FIRST" > version
```

Add that file to git:

```
git add version
```

Create a new commit:

```
git commit -am "Version number 1"
```

Now tag that commit with tag "1":

```
git tag 1
```

You have now created the first immutable version of code for your 'version' file.

Now let's create version 2.

Modify your 'version' file to have just one line with "SECOND"

```
echo "SECOND" > version
```

Create a new commit:

```
git commit -am "Version number 2"
```

Now tag that commit with tag "2":

```
git tag 2
```

You have now created the second immutable version of code for your 'version' file.

And finally let's repeat the process for the third version of this file.

Modify your 'version' file to have just one line with "THIRD"

```
echo "THIRD" > version
```

Create a new commit:

```
git commit -am "Version number 3"
```

Now tag that commit with tag "3":

```
git tag 3
```

You have now successfully created your 3 immutable versions of code for your 'version' file.

Check your available git tags:

```
git tag
```


With this you can now switch among the different versions of code using:

```
git checkout <tag>
```

Switching among a number of different versions of a file is really useful in many different scenarios. For example you could have a Dockerfile for a demonstration, and want to show how a deployment works while increasing the number of containers in phased steps.

Additionally, if you Run Visual Studio Code and open your 'version' file, you will see its content automatically changing when you run `git checkout <tag>` from your terminal.

Ain't that cool??
