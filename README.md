# Git hooks - Automating daily tasks

## prepare-commit-msg

Git definition:
The prepare-commit-msg hook is run before the commit message editor is fired up but after the default message is created. It lets you edit the default message before the commit author sees it. [Continue reading...](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks)

## Setup

Inside of any git init or clone folder, you will have the following path already created: `.git/hooks`, it contains all the available hooks that Git provide us.

To activate them, you just need to rename the file name `*.sample`, in our case we need the hook `prepare-commit-msg.sample` which you need to rename to `prepare-commit-msg` and copy the hook from our repo (yes this, is also yours).

And this is everything, this folder is ignored by default, this behaviour is intended to give autonomy to any developer/engineer. Now, the possibilities here are limitless, just you are going to be the limit!

## Usage

We are now taking this hook to automate the tedious task of writing all the time the same types and issue number `type(TICKET-999): finally writing my commit` and instead read it from the branch directly.

Branch name: `bug/JIRA-999/sentry-crazy-bug`

```
$ git commit -m 'this will solve the bug'
```

output: `bug(JIRA-999): this will solve the bug`

If you prefer to go the vim way: \
Branch name: `bug/JIRA-999/sentry-crazy-bug`

```
$ git commit
```

```
[VIM] press SHIFT + A to start typing at the end of the line, I added a space.
bug(JIRA-999): // here you can start typing
```
