## 服务器分析

服务器.zip文件目录：

```
比武虚拟机
	- vmware.log
	- vmware-0.log
	- vmware-1.log
	- 金华WA服务器比武.nvram
	- 金华WA服务器比武.vmdk
	- 金华WA服务器比武.vmsd
	- 金华WA服务器比武.vmx
	- 金华WA服务器比武.vmxf
	- 金华WA服务器比武-s001.vmdk
	- 金华WA服务器比武-s002.vmdk
	- 金华WA服务器比武-s003.vmdk
	- 金华WA服务器比武-s004.vmdk
```

### 0、仿真

#### 爆破root密码

拿到镜像，首先看到vmdk虚拟机文件，明显可以使用VMware打开，直接仿真分析。

**但root密码未知，无法成功进入！**

而且磁盘文件被分成了多个，使用`FTK Imager`等工具无法全部识别。

<img src=".\image\image-20240131140349192.png" alt="image-20240131140349192" style="zoom:80%;" />

**使用`vmware-vdiskmanager.exe`工具将多个`-s00*.vmdk`文件合并**

> `vmware-vdiskmanager.exe`是VMware虚拟机自带的工具，可在`\VMware\VMware Workstation`目录找到

<img src=".\image\image-20240131140503476.png" alt="image-20240131140503476" style="zoom:80%;" />

> **取证大师**可以直接添加所有文件镜像，不需要手动合并

之后使用`FTK Imager`工具可打开文件目录：

<img src=".\image\image-20240131140647299.png" alt="image-20240131140647299" style="zoom:80%;" />

在Linux的文件系统中，`/etc/shadow`文件保存了用户信息，可以看到主要是root用户、a用户存在密码，**使用工具爆破得到root用户密码为`qwer1234`**，即可正常仿真进入系统。

> `kali`中存在`john`工具，`--wordlist`可指定字典
>
> `a`用户的密码并不重要。

<img src=".\image\image-20240131141157932.png" alt="image-20240131141157932" style="zoom:80%;" />

#### 图形化界面

VMware选择`金华WA服务器比武.vmx`文件可打开镜像，初始配置如下：

<img src=".\image\image-20240131141833000.png" alt="image-20240131141833000" style="zoom:80%;" />

图形化界面需要选择（`0-rescue-**`）：

<img src=".\image\image-20240131141924214.png" alt="image-20240131141924214" style="zoom:80%;" />

但由于初始配置不够无法进入图形化界面，可修改配置中的处理器数量为2即可

