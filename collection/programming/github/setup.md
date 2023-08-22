
This setup is what I use. It assumes you are either using Linux/Mac (bash) or Git Bash on Windows.

<br>

---

<br>

## Username & Email

<br>

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

<br>

---

<br>

## Set VSCode as Git Editor

<br>

This assumes that code is set in PATH.

```bash
git config --global core.editor "code --wait"
```

<br>

---

<br>

## Set SSH

<br>

#### Check Existing SSH Keys

```bash
ls -al ~/.ssh
```

<br>

#### Start ssh-agent

```bash
eval "$(ssh-agent -s)"
```

<br>

#### Add SSH Key to Agent

```bash
ssh-add
```

<br>

---

<br>

## Set GPG Key

<br>

This assumes that you [Set up GPG for Git](https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key)

<br>

1. Get the GPG Key:

```bash
gpg --list-secret-keys --keyid-format LONG
```

<br>

2. Set the GPG:

```bash
git config --global user.signingkey YOURKEYID
git config --global commit.gpgsign true
```

<br>

3. Windows Only:

```bash
git config --global gpg.program "C:/Program Files (x86)/GnuPG/bin/gpg.exe"
```

<br>

4. Set GPG agent (timeout):

- Open the `gpg-agent.conf` file in a text editor. If the file does not exist, create it.
- Add the following lines to the file (365 days):

```bash
default-cache-ttl 31536000 
max-cache-ttl 31536000
```

<br>

5. Reset GPG Agent:

```bash
gpg-connect-agent reloadagent /bye
```