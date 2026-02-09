## Git File Lifecycle

```text
+-------------------+
| Working Directory |
| (modified files)  |
+-------------------+
          |
          | git add (to stage the files from working directory)
          v
+-------------------+
| Staging Area      |
| (index)           |
+-------------------+
          |
          | git commit (only add staged files to repo )
          v
+-------------------+
| Repository        |
| (commit history)  |
+-------------------+
```
