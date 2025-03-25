---
alias: 配置 Github SSH
---

# 配置 Github SSH

在访问 Github 仓库时，通常推荐使用 SSH 的方式，其带来的好处是：

1. **安全性**：SSH 使用加密的方式传输数据，确保数据在传输过程中不会被窃取或篡改。
2. **免密码登录**：配置 SSH 密钥后，可以免密码登录 GitHub，提高了使用的便利性。
3. **身份验证**：SSH 密钥是基于公钥和私钥的身份验证机制，安全性更高。

相比之下，HTTP 方式虽然也可以使用，但需要每次操作时输入用户名和密码，安全性和便利性都不如 SSH 方式。本文将讲述如何配置 GitHub SSH，其主要步骤包括：
1. 本地创建 SSH Key 对
2. 将 SSH Key 添加到 GitHub 账户
3. 使用示例工程测试 SSH 配置是否成功


## 本地创建 SSH Key 对

在命令行中运行 `ssh-keygen` 命令，按照提示输入文件名和密码，即可生成 SSH Key 对：

```bash
ssh-keygen -t ed25519 -C <email>
# 如 ssh-keygen -t ed25519 -C dumnmyuser@outlook.com
```

在命令执行过程中，会有一系列的选项，如设置 ssh key 生成的地址、密码等，这里建议都不进行设置降低复杂度。生成成功后，可以在 `~/.ssh/` 目录下看到生成的 SSH Key 对，一般包括两个文件：`id_ed25519` 和 `id_ed25519.pub`，分别是私钥和公钥。

打开 `id_ed25519.pub` 文件，将其中的内容复制到剪贴板，后续需要将其添加到 GitHub 账户中。

> [!tip]
>
> 在 Windows 系统中，`~/.ssh/` 目录为 `C:\Users\<username>\.ssh\` 。

## 将 SSH Key 添加到 GitHub 账户

登录 GitHub 账户，点击右上角头像，选择 `Settings` 进入设置页面：
![Github Settings ](assets/Config%20Github%20SSh/2025-03-25-15-00-00.png)

在设置页面中，选择 `SSH and GPG keys`，点击 `New SSH key`：
![New SSH Key](assets/Config%20Github%20SSh/2025-03-25-15-01-57.png)

在 `Add new SSH Key` 界面，你需要填入 `Title` 和 `Key`，其中 `Title` 可以随意填写，Title 用于标识该 SSH Key，在 Key 处填入前面生成的 `id_ed25519.pub` 文件的内容，然后点击 `Add SSH key` 即可。
![Add new SSH Key](assets/Config%20Github%20SSh/2025-03-25-15-13-49.png)

## 测试 SSH 配置是否成功

当完成上述步骤后， SSH 已经成功配置，你可以挑选任意的 Public Github 工程进行 ssh clone 测试，如针对项目 `PlayForDreamDevelopers/support`，你应当找到他的 ssh 地址并进行 clone 操作：
![SSH URL](assets/Config%20Github%20SSh/2025-03-25-15-17-29.png)

```bash
git clone git@github.com:PlayForDreamDevelopers/support.git
```

# FAQ

## 在进行 Clone 时提示 Timeout 怎么办

如果在进行 Clone 操作时提示 Timeout，可能是由于网络问题导致的，可以尝试配置本地代理解决，在 `~\.ssh` 目录下添加 `config` 文件，并在 `~\.ssh\config` 中配置代理：
```bash
Host github.com
	Hostname ssh.github.com
	User git
	Port 443
    	ProxyCommand connect -H <LocalPath:Port> %h %p
```

其中的 `LocalPath:Port`，如你使用 `Clash` 其通常为 `127.0.0.1:7890`
