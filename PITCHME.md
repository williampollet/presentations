## Automatic code reviews with pronto

![image](assets/images/speedy_gonzales.png)

---

### introduction: RuboCop in theory

 - raise an offense for each style error
 - Allow the team to build and share a common codestyle through the `rubocop.yml`

---

### Motivation: RuboCop in practice

![image](assets/images/offenses-kisskiss.png)

---

![image](assets/images/broken-window-theory.jpg)

---

![image](assets/images/broken-window-building.jpg)

---

### pronto

Execute `RuboCop` _only_ on the diffs between your branch and master

---

### install it

```bash
$ gem install pronto
$ gem install pronto-rubocop
$ gem install pronto-eslint
```

---

### Run it locally
```bash
$ pronto run
```

---

### Results

![image](assets/images/offenses-local-branch.png)

 - You don't see the broken windows anymore
 - you have a reasonable number of offenses to deal with

---

### Still...

Frictions are staying for the codestyle build

---

### Automatic code reviews

```bash
$ pronto run -f github_pr_review
```

---

### github_pr_review setup 1/2

Create a `pronto.yml`:
```yml
github:
  slug: KissKissBankBank/kisskissbankbank
github_pr_review:
  format: "%{msg}"
max_warnings: 200
verbose: false
```

---

### github_pr_review setup 2/2

Provide:
 - A Github personal_access_token
 - the number of the PR you want pronto to review

---

### How do we use it at kisskiss?

Meet the Kissbot :)
![image](assets/images/meet-the-kissbot.png)

---

### Why the kissbot? 1/2

![image](assets/images/kissbot-slack-conversation.png)

---

### Why the kissbot? 2/2

![image](assets/images/kissbot-comments.png)

---

### Conclusion
