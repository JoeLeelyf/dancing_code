# tmux
终端复用工具。利用tmux可以轻松创建、管理多个终端会话，实现在单个终端窗口中同时访问多个终端会话。并在本地和远程服务器断连之后能够保持终端会话不中断，保持原进程一直在服务器中运行，再下次连接服务器时仍能进入原来会话。
## 安装
```bash
sudo apt install tmux
```
## 基本概念
### 会话 (session)
tmux的基本单位是会话（session），一个会话可以包含多个窗口（window），一个窗口可以包含多个窗格（pane）。
### 窗口 (window)
窗口是一个独立的工作区域，可以在其中运行一个或多个程序。窗口可以水平或垂直分割成多个窗格，每个窗格都是一个独立的终端。
### 窗格 (pane)
窗格是窗口的一个子区域，窗格是一个独立的终端，可以在其中运行一个或多个程序。
<img src="https://pic4.zhimg.com/v2-c117e59e1de94709ae889dc59119d6cb_r.jpg">

## 基本操作
1. 会话管理：
- tmux : 创建一个新的tmux会话。
    - tmux new -s session-name: 创建一个新的tmux会话，并指定会话名称。
    - tmux new -s session-name -d: 创建一个新的tmux会话，并指定会话名称，但不连接到该会话。
    - tmux rename-session -t old-name new-name: 重命名一个tmux会话。
- tmux attach -t target_session: 连接到一个已存在的tmux会话。
- tmux switch -t target-session: 切换到指定的tmux会话。
- tmux list-sessions: 列出所有的tmux会话。
- tmux detach /Crtl-b d: 断开与当前会话的连接。
1. 窗口管理：
- Ctrl-b c（按下Ctrl和b键，然后松开，再按下c键）: 创建一个新窗口。
- Ctrl-b n: 切换到下一个窗口。
- Ctrl-b p: 切换到上一个窗口。
- Ctrl-b l: 在最后两个窗口之间切换。
- Ctrl-b 0-9: 切换到特定编号的窗口。
- Ctrl-b ,（逗号）: 重命名当前窗口。
1. 面板管理：
- Ctrl-b %: 创建一个新的垂直面板。
- Ctrl-b "（双引号）: 创建一个新的水平面板。
- Ctrl-b 方向键: 在面板间切换焦点。
- Ctrl-b x: 关闭当前面板。
- Ctrl-b z: 最大化或还原当前面板。
1. 其他操作：
- Ctrl-b d: 断开当前tmux会话，返回到终端。
- Ctrl-b ?: 显示tmux快捷键帮助。
- Ctrl-b :（冒号）: 进入命令模式，可以执行tmux命令。