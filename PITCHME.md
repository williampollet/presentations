## Automatic code reviews with pronto

<img src="assets/images/speedy_gonzales.png" style="width: 30%; border: 0;" />

---

## introduction
### RuboCop in theory

 - raise an offense for each style error
 - Allow the team to build and share a common codestyle through the `rubocop.yml`

---

## Motivation
### RuboCop in practice

![image](assets/images/offenses-kisskiss.png)

---

<img src="assets/images/broken-window.jpg" style="width: 60%; border: 0;" />

---

<img src="assets/images/broken-window-building.jpg" style="width: 60%; border: 0;" />

---

### The pronto gem

Executes `RuboCop` _only_ on the diffs between your branch and master

---

### install it

```bash
$ gem install pronto
$ gem install pronto-rubocop
$ gem install pronto-eslint
```

---

### Run it locally

![image](assets/images/offenses-local-branch.png)

 - no broken windows left by others
 - reasonable number of offenses to deal with

---

### Still...

Frictions stay to build and share the codestyle

---

### Automatic code reviews

```bash
$ pronto run -f github_pr_review
```

---

### github pr review setup 1/2

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

### github pr review setup 2/2

Provide:
 - A Github `personal_access_token`
 - the `id` of the PR you want pronto to review

---

### How do we use it at kisskiss?

![image](assets/images/meet-the-kissbot.png)

---

### Why the kissbot? 1/2

<img src="assets/images/kissbot-comments.png" style="width: 30%; border: 0;" />

---

### Why the kissbot? 2/2

<img src="assets/images/kissbot-slack-conversation.png" style="width: 30%; border: 0;" />

---

### Conclusion

---

<img src="assets/images/speedy_gonzales_bye.png" style="width: 30%; border: 0;" />
