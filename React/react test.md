Yes — in Git Bash, Windows paths use `/` not `\`.

Use this:

```bash
cd /c/Users/sudha/OneDrive/Desktop/ss
```

### Why?

Windows path:

```txt
C:\Users\sudha\OneDrive\Desktop\ss
```

Git Bash format:

```txt
/c/Users/sudha/OneDrive/Desktop/ss
```

* `C:` becomes `/c`
* `\` becomes `/`

Then check files:

```bash
ls
```

And check current folder:

```bash
pwd
```
