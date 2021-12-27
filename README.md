# Emoji Commits


### PHILOSOPHY

In order to reduce inconsistencies with work commits, and to provide a uniform system that is visually easy to understand, emoji commits was modified to fir the organization needs. 

1. **IMPERATIVE** ↓

    - Make your Git commit messages imperative.
    - Write a commit message like you're giving an order.
    - E.g., Use ✅ `Add` instead of ❌ `Added`.
    - E.g., Use ✅ `Create` instead of ❌ `Creating`.
    
2. **RULES** ↓

    - A small number of categories — easy to memorize.
    - Nothing more nothing less.
    - E.g. `📦 NEW`, `👍 IMPROVE`, `🐛 FIX`, `📖 DOCUMENT`, `🚀 READY`, `🤖 TESTING`, and `☣️ BREAKING`
    
3. **ACTIONS** ↓

    - Make git commits based on the actions you take.
    
### GETTING STARTED

Only use the following Git Commit Messages. A simple and small footprint is critical here.

1. `📦 NEW: IMPERATIVE_MESSAGE_GOES_HERE`
    > Use when you add something entirely new.
    > E.g. `📦 NEW: Add Git ignore file`

1. `👍 IMPROVE: IMPERATIVE_MESSAGE_GOES_HERE`
    > Use when you improve/enhance piece of code like refactoring etc.
    > E.g. `👌 IMPROVE: Remote IP API Function`

1. `🐛 FIX: IMPERATIVE_MESSAGE_GOES_HERE`
    > Use when you fix a bug — need I say more?
    > E.g. `🐛 FIX: Case conversion`

1. `📖 DOCUMENT: IMPERATIVE_MESSAGE_GOES_HERE`
    > Use when you add documentation like `README.md`, or even inline docs.
    > E.g. `📖 DOC: API Interface Tutorial`

1. `🚀 READY: IMPERATIVE_MESSAGE_GOES_HERE`
    > Use when you release a new version.
    > E.g. `🚀 RELEASE: Version 2.0.0`

1. `🤖 TESTINT: IMPERATIVE_MESSAGE_GOES_HERE`
    > Use when it's related to testing.
    > E.g. `🤖 TEST: Mock User Login/Logout`

1. `☣️ BREAKING: IMPERATIVE_MESSAGE_GOES_HERE`
    > Use when releasing a change that breaks previous versions.
    > E.g. `‼️ BREAKING: Change authentication protocol`

### GIT ALIASES

- `git inc` => Takes no message and is for the initial commit ONLY => `🎉 INITIAL COMMIT`
- `git fb <branch-name>` => Take a branch name and creates a `feature/branch` and set the upstream to that branch
- `git new '<message>'` => Take a commit message, and uses `git cap` to add, commit, and push => `📦 NEW: <message>`
- `git imp '<message>'` => Take a commit message, and uses `git cap` to add, commit, and push => `👍 IMPROVE: <message>`
- `git fix '<message>'` => Take a commit message, and uses `git cap` to add, commit, and push => `🐛 FIX: <message>`
- `git rdy '<message>'` => Take a commit message, and uses `git cap` to add, commit, and push => `🚀 READY: <message>`
- `git doc '<message>'` => Take a commit message, and uses `git cap` to add, commit, and push => `📖 DOCUMENT: <message>`
- `git tst '<message>'` => Take a commit message, and uses `git cap` to add, commit, and push => `🤖 TESTING: <message>`
- `git brk '<message>'` => Take a commit message, and uses `git cap` to add, commit, and push => `☣️ BREAKING: <message>`
- `git cap '<message>'` => Take a commit message, to add, commit, and push 

### GITCONFIG UPDATE

- Update your gitconfig file with the following codesnippet
- `code ~/.gitconfig`


```js
[init]
	defaultBranch = main
[alias]
  # Git Commit, Add all and Push — in one step.
  cap = "!f() { git add .; git commit -m \"$@\"; git push; }; f"
  # NEW.
  new = "!f() { git cap \"📦 NEW: $@\"; }; f"
  # IMPROVE.
  imp = "!f() { git cap \"👍 IMPROVE: $@\"; }; f"
  # FIX.
  fix = "!f() { git cap \"🐛 FIX: $@\"; }; f"
  # READY.
  rdy = "!f() { git cap \"🚀 READY: $@\"; }; f"
  # DOCUMENT.
  doc = "!f() { git cap \"📖 DOCUMENT: $@\"; }; f"
  # TESTING.
  tst = "!f() { git cap \"🤖 TESTING: $@\"; }; f"
  # BREAKING CHANGE.
  brk = "!f() { git cap \"☣️ BREAKING: $@\"; }; f"
  # Feature branch.
  fb = "!f() { git checkout -b "feature/$@"; git push -u origin "feature/$@"; }; f"
  # Initial commit. 
  inc = "!f() { git add .; git commit -m \"🎉 INITIAL COMMIT\"; git push -u origin main; }; f"
```

### Credits

- Emoji Commits is a modified version of Emoji-Logs. 
