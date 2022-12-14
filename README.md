## **covermytracks - Tool for pentesters.**
![whole-house-carpet-cleaning-logo](https://user-images.githubusercontent.com/90393971/188179794-783ffbe5-589d-4fa0-b8f3-d239638294c8.png)

#### **Shell script to cover your tracks on UNIX systems. Designed for pen testing covering tracks phase, before exiting the infected server. Or, permanently disable system logs for post-exploitation.**

#### **Installation**

#### **With sudo :**

```bash
sudo curl -sSL https://raw.githubusercontent.com/sagarkhandve/covermytracks/main/covermytracks -o /usr/bin/covermytracks
sudo chmod +x /usr/bin/covermytracks
```

#### **Without sudo :**

```bash
mkdir -p .local/bin
curl -sSL https://raw.githubusercontent.com/sagarkhandve/covermytracks/main/covermytracks -o ~/.local/bin/covermytracks
chmod +x ~/.local/bin/covermytracks
```

#### **You can now use the tool using the executable.**

#### **Keep in mind that without sudo privileges, you *might* be unable to clear system-level log files (`/var/log`).**

#### **Usage :**

```
covermytracks # you may need to use sudo if you want to clean auth logs
```

#### **Follow the instructions :**
```
Welcome to covermytracks!

Select an option :
1) Clear logs for user root
2) Permenently disable auth & bash history
3) Restore settings to default
99) Exit tool

>
```

#### **NOTE: don't forget to exit the terminal session since the bash history is cached.**

#### **Clear logs instantly (requires *sudo* to be efficient) :**

```
sudo covermytracks now
```

#### **Job scheduler using cron job. Clear bash history every day at 6am :**

```bash
0 6 * * * covermytracks now >/dev/null 2>&1
```
## 
[![License](https://img.shields.io/badge/LICENSE-MIT-blue?style=flat-square&logo)](#license "Go to license section")
