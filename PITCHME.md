## Automatic code reviews with `Pronto`

<img src="assets/images/speedy_gonzales.png" style="width: 30%;" />

---

## `RuboCop` in theory

 - Code without style error

 - Build a team codestyle with the `rubocop.yml`

---

## `RuboCop` in practice

![image](assets/images/offenses-kisskiss.png)

---

<img src="assets/images/broken-window.jpg" style="width: 70%;" />

---

<img src="assets/images/broken-window-building.jpg" style="width: 70%;" />

---

## `Pronto`

Executes `RuboCop` _only_ on the diffs between your branch and master

---

## installation

```bash
$ gem install pronto
$ gem install pronto-rubocop
$ gem install pronto-eslint
```

---

## Local run

![image](assets/images/offenses-local-branch.png)

 - no broken windows visible

 - reasonable number of offenses to deal with

---

## Still

Frictions remains for building the team codestyle

---

## github pr review

Create a `pronto.yml` file:
```yml
github:
  slug: YourOrg/YourRepo
github_pr_review:
  format: "%{msg}"
max_warnings: 200
verbose: false
```

---

## github pr review

 - provide a Github `personal_access_token` (with repo rights)
```bash
$ PRONTO_GITHUB_ACCESS_TOKEN=********
```

 - provide the `id` of the PR you want `Pronto` to review
```bash
$ PULL_REQUEST_ID=10
```

---

## github pr review
##### use it

```bash
$ pronto run -f github_pr_review -c origin/master
```

---


## Meet the KissBot

![image](assets/images/meet-the-kissbot.png)

---

<img src="assets/images/kissbot-comments.png" style="width: 70%;"/>

---

<img src="assets/images/kissbot-slack-conversation.png" style="width: 80%;" />

---

## Conclusion

---

<img src="assets/images/speedy_gonzales_bye.png" style="width: 40%;"/>
