# CVE
2026-31431
bash fix_cve-2026-31431-en.sh or sh fix_cve-2026-31431-en.sh
==================================================================
  CVE-2026-31431 (Copy Fail) Vulnerability General Detection and Remediation Script
==================================================================
[1/4] Checking system vulnerability status...
modprobe: unrecognized option: -
  [WARNING] Module algif_aead is loaded and running, system is at risk of privilege escalation!

[2/4] Checking if the module is currently being used by applications...
cve-2026-31431.sh: line 41: ss: not found
  [OK] No applications are currently calling this module.

[3/4] Performing environment backup...
  [INFO] The system currently has no relevant configuration files, initial state recorded.

[4/4] Preparing to execute vulnerability remediation
==================================================================
!!! WARNING !!!
This operation will completely disable and attempt to unload the algif_aead module from memory.
Before executing, please ensure you have taken a [Snapshot] or [Full Backup]
of the server at the infrastructure level (e.g., vCenter / Proxmox / Cloud Console).
==================================================================
If you confirm that the backup/snapshot is complete, enter 'ConFirm' to execute the fix: ConFirm

Starting remediation...
cve-2026-31431.sh: line 95: can't create /etc/modprobe.d/disable-algif_aead.conf: nonexistent directory
  [√] Blocklist rule written: /etc/modprobe.d/disable-algif_aead.conf
  [√] Successfully unloaded algif_aead module from memory, blocking the vulnerability immediately.
  中文
  ==================================================================
  CVE-2026-31431 (Copy Fail) 漏洞通用检测与修复脚本
==================================================================
[1/4] 检查系统漏洞状态...
  [INFO] 模块当前未运行，但未被配置为禁用，存在被恶意程序唤醒的风险。

[2/4] 检查模块是否正在被应用使用...
  [OK] 当前没有任何应用在调用该模块。

[3/4] 执行环境备份...
  [INFO] 系统当前无相关配置文件，已记录初始状态。

[4/4] 准备执行漏洞修复
==================================================================
!!! 警告 !!!
该操作将彻底禁用并尝试从内存中卸载 algif_aead 模块。
执行前，请务必确认您已经在底层（如 vCenter / Proxmox / 云控制台）
针对该服务器做好了【快照】或【完整备份】。
==================================================================
如果您确认已完成备份/快照，请输入 'ConFirm' 以执行修复: ConFirm

开始执行修复...
  [√] 已写入底层禁用规则: /etc/modprobe.d/disable-algif_aead.conf
  [INFO] 检测到 update-initramfs 工具，正在更新内核启动镜像 (预计需要 1-2 分钟)...
  [√] 内核启动镜像更新完成。
