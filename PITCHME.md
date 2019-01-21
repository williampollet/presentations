# Safepush

Reduce the feedback loop on your tests and linters results

---

### @css[head](Use case)

Oftenly as a software developer, I guess you are confronted to this scenario

<img src="assets/images/circle_fail.png" style="width: 100%;" />

Note:
 - This is just saying that your tests failed on the CI

---

### Why does it matter ?

<img src="assets/images/should_i_care.jpg" style="width: 50%;" />

Note:
 - Now you are probably telling yourself, ok, and so what ? (spéciale cassdédi à AnneSo)

---

### Let's have a look at the relevant information here

<img src="assets/images/circle_fail_info.png" style="width: 100%;" />

Note:
What does those 12ish min means ? Tip : this is a problem. To understand why, let's dig into the context:
 - you just finished your development on your local branch. Proud of your code, you push on Github and open a pull request.
 - If the codebase is consequent (which is the case at Kisskiss) you have the output of the CI approximately 20 mins after you opened your PR.
 - 20 min is a long time if you wait and thus it is just about the minimal time you need to concentrate effectively on a task.
 - This chopped process results in a tremendous productivity loss if you have no bypass strategies: the development

---

### Bypass strategies

- Fire and forget
- Reducing the feedback loop

Note:
 - F&F : work on an other issue after you pushed, come back on this one later on
 - Reducing the feedback loop : testing on your local, only the files you modified

---

### Strategy 1

- Useful the first time you send your code
- Less useful when want to make quick iterations
- Less useful when you need to iterate on one pull request over time

---

### Strategy 2: Introducing SafePusher

A command line allowing you to test and run the linters only on the files you modified, to reduce your feedback loop.

Note:
- the other strategy is to test in local, by selecting only the changes you made to avoid having to wait for the complete test suite to pass.

---

### Installation

```bash
  $ gem install safe_pusher
```

---

### Configuration

```yml
files_to_skip:
  - file/to/skip_1
  - file/to/skip/2
app_base_directory: app
repo_url: https://github.com/williampollet/safe_pusher
```

---

### Usage

```bash
  $ safepush test lint push open
  $ safepush p o
```

Note:
 - you can execute the commands you wish between test, push, open and lint

---

### Alternatives

- [Guard](https://github.com/guard/guard)

---
