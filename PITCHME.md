## Get back in time with git reflog

Shit git, I did something terribly wrong. What can I do?

Note:

---

## First solution: git checkout #sha1

```bash
  git lg
  git checkout e3bbi34
  git lg
```

---

## So why git reflog?

What happens when I do something terribly wrong? like a `reset --hard` ?

---

## Git Reflog: the git time machine

```bash
  git reflog
```

---

# Demo time

---

# The magic of git Reflog

You will _never make irreversible changes_ anymore.
