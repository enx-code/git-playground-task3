# Unit 4 Git playground — Lesson 3

A tiny command-line notes tool, used as the practice repo for Unit 4, Lesson 3 (branches and pull requests). You'll make one small change, then let Claude put it on a branch and open a pull request for you — with a description that actually explains what you did.

### The app
- `node notes.js add <text>` — add a note
- `node notes.js list` — list all notes
- `node notes.js search <term>` — list notes containing a term
- `node notes.js edit <id> <new text>` — change the text of a note
- `node notes.js delete <id>` — delete a note

Layout: `notes.js` is the entry point, `lib/store.js` loads, saves, and searches notes, `lib/config.js` holds settings, and `tests/` holds the test suite (`npm test`).

### Set up
1. Make sure you have your own copy of this repo (created from the lesson on the platform).
2. Clone it locally, and run `gh auth login` so Claude can open pull requests through the `gh` CLI.
3. Open Claude Code in the folder.

### Lesson 3 task — let Claude branch and open the PR
Goal: make a small change, then have Claude put it on a new branch and open a pull request whose description reflects what actually changed.

1. **Check the starting point.** Run `npm test`. Everything passes — that's a healthy `main`.
2. **Make one small change.** For example, add a `count` command that prints how many notes you have (`node notes.js count` → `You have 3 notes.`). You can write it yourself or ask Claude to. Or make a small change of your own.
3. **Confirm it still works.** Run `npm test` again — a change worth a pull request shouldn't break the build.
4. **Put it on a branch.** Ask Claude: *"Put my change on a new branch and commit it."* Claude keeps `main` clean and does the work on a branch.
5. **Open the pull request.** Ask Claude: *"Open a pull request for this branch. Select mate-academy/git-playground-task3 as a base"* It reads your commits and writes the title and description.
6. **Read what Claude wrote.** Open the PR on GitHub. Does the description explain *what* changed and *why* — and flag anything a reviewer should check?
7. **Open** the pull request against the main repository, not your fork. CI runs your tests on the PR — it should come back green.
