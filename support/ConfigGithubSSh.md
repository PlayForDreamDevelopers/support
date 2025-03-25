# Configure GitHub SSH

When accessing GitHub repositories, it is generally recommended to use SSH for the following benefits:

1. **Security**: SSH uses encryption to transmit data, ensuring that the data is not intercepted or tampered with during transmission.
2. **Password-free login**: After configuring the SSH key, you can log in to GitHub without a password, improving convenience.
3. **Authentication**: SSH keys use a public and private key authentication mechanism, which is more secure.

In contrast, although the HTTP method can also be used, it requires entering a username and password for each operation, making it less secure and convenient than SSH. This article will explain how to configure GitHub SSH, including the following main steps:
1. Create an SSH key pair locally
2. Add the SSH key to your GitHub account
3. Test the SSH configuration with a sample project

## Create an SSH Key Pair Locally

Run the `ssh-keygen` command in the command line and follow the prompts to enter the file name and password to generate an SSH key pair:

```bash
ssh-keygen -t ed25519 -C <email>
# e.g., ssh-keygen -t ed25519 -C dummyuser@outlook.com
```

During the command execution, there will be a series of options, such as setting the address and password for the SSH key. It is recommended to skip these settings to reduce complexity. After successful generation, you can find the SSH key pair in the `~/.ssh/` directory, usually consisting of two files: `id_ed25519` and `id_ed25519.pub`, which are the private key and public key, respectively.

Open the `id_ed25519.pub` file and copy its contents to the clipboard. You will need to add it to your GitHub account later.

> [!tip]
>
> On Windows, the `~/.ssh/` directory is `C:\Users\<username>\.ssh\`.

## Add the SSH Key to Your GitHub Account

Log in to your GitHub account, click on your avatar in the upper right corner, and select `Settings` to enter the settings page:
![GitHub Settings](assets/Config%20Github%20SSh/2025-03-25-15-00-00.png)

On the settings page, select `SSH and GPG keys` and click `New SSH key`:
![New SSH Key](assets/Config%20Github%20SSh/2025-03-25-15-01-57.png)

In the `Add new SSH Key` interface, you need to fill in the `Title` and `Key`. The `Title` can be anything you like, used to identify the SSH key. In the `Key` field, paste the contents of the `id_ed25519.pub` file generated earlier, and then click `Add SSH key`.
![Add new SSH Key](assets/Config%20Github%20SSh/2025-03-25-15-13-49.png)

## Test the SSH Configuration

After completing the above steps, SSH has been successfully configured. You can select any public GitHub project to test the SSH clone, such as the project `PlayForDreamDevelopers/support`. Find its SSH address and perform the clone operation:
![SSH URL](assets/Config%20Github%20SSh/2025-03-25-15-17-29.png)

```bash
git clone git@github.com:PlayForDreamDevelopers/support.git
```

# FAQ

## What to Do If Timeout Occurs During Clone

If a timeout occurs during the clone operation, it may be due to network issues. You can try configuring a local proxy to resolve this. Add a `config` file in the `~/.ssh` directory and configure the proxy in `~/.ssh/config`:

```bash
Host github.com
    Hostname ssh.github.com
    User git
    Port 443
    ProxyCommand connect -H <LocalPath:Port> %h %p
```

For `LocalPath:Port`, if you are using `Clash`, it is usually `127.0.0.1:7890`.