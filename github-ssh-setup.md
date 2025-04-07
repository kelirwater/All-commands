# 🔐 SSH Key Setup for GitHub

Setting up an SSH key allows you to securely connect to GitHub without entering your username and password each time.

---

## 📌 `ssh-keygen`

**Definition:** Generates a new SSH key.

**Example:**

```bash
ssh-keygen -t ed25519 -C "your-email@chaicode.com"
```

- `-t ed25519`: Specifies the key type (recommended).
- `-C`: A comment label, usually your email address.

---

## 💾 Saving the Key

After running the above command, you'll see a prompt:

```bash
Enter a file in which to save the key (/Users/YOU/.ssh/id_ed25519): [Press enter]
```

- Press **Enter** to accept the default location.
- When prompted, optionally enter a **passphrase** or press Enter to skip.

---

## ⚙️ `ssh-agent`

**Definition:** A program that keeps your private key in memory for secure access.

### Start the agent:

**macOS / Linux:**

```bash
eval "$(ssh-agent -s)"
```

**Windows (Git Bash):**

```bash
eval $(ssh-agent -s)
```

### Add your private key:

```bash
ssh-add ~/.ssh/id_ed25519
```

> 💡 **macOS only:** Add your SSH key to the keychain:

```bash
ssh-add --apple-use-keychain ~/.ssh/id_ed25519
```

---

## 📋 Copy Public Key to Clipboard

### macOS:

```bash
pbcopy < ~/.ssh/id_ed25519.pub
```

### Windows (Git Bash):

```bash
clip < ~/.ssh/id_ed25519.pub
```

### Linux:

```bash
xclip -sel clip < ~/.ssh/id_ed25519.pub
```

---

## ➕ Add SSH Key to GitHub

1. Go to: [GitHub → Settings → SSH and GPG Keys](https://github.com/settings/keys)
2. Click **"New SSH Key"**
3. Add a **title** (e.g., `My MacBook`) and paste the copied public key
4. Click **"Add SSH key"**

👉 More info: [GitHub Docs – Add a new SSH key](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)

---

## ✅ Test the SSH Connection

**Run:**

```bash
ssh -T git@github.com
```

**Expected output:**

```bash
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```

---

## 📚 References

- [GitHub Docs – Connecting to GitHub with SSH](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)
- [GitHub Docs – Adding a new SSH key](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)

You can also check the [Git Commands Documentation](./Git_Commands.md) for more details on using Git in PowerShell and Command Prompt.
