# claude+idea实现Java接口级别代码安全审计

## 前置条件
- 1、本地安装并配置好Claude code （免登陆即可）
- 2、idea安装Claude插件
- 3、配置本skill（audit-tracer）

## 详细步骤
### 安装配置Claude
- 本步骤略
### 安装Claude插件
- 插件市场搜索claude，选择安装图中插件，会自动连上本机已安装的Claude
  
<img width="983" height="735" alt="image" src="https://github.com/user-attachments/assets/47bed552-23a5-40b2-aff6-c6e3e575418f" />



### 打开idea claude插件
- 直接点击右上角图标即可
<img width="520" height="220" alt="image" src="https://github.com/user-attachments/assets/d33a42f9-555b-4473-8e66-7ae8c5ad023e" />


### 配置本skill
- 将本skill复制到Claude的skills目录即可
<img width="665" height="285" alt="image" src="https://github.com/user-attachments/assets/c7f02dbc-b39a-4cf7-be2b-78baadd2a459" />


### 使用本skill
- / 唤起，tab选中
<img width="729" height="171" alt="image" src="https://github.com/user-attachments/assets/0d83e50a-8fc6-48c1-939c-f1adf6949c29" />

- 然后选中需要审计的接口，点击图标发送至Claude窗口
<img width="881" height="221" alt="image" src="https://github.com/user-attachments/assets/1fa1eeeb-b173-4efd-adc8-3c1d58cb158e" />

- 添加指令：审计当前接口（类似皆可）
<img width="735" height="120" alt="image" src="https://github.com/user-attachments/assets/4b98ac4c-41f8-4c30-a747-7ec45713ea5c" />

- 回车，即可开始审计。
- 但是需要注意，在进行追踪调用链后，如果业务流程较长，可能需要手动确认是否继续追踪其它调用链，本skill默认仅往下追踪5层。

### 效果图
- 此时可结合报告，对源代码进行代码安全审查
<img width="1831" height="905" alt="image" src="https://github.com/user-attachments/assets/a9ae763c-ca33-4c44-acce-25594da5c084" />

## 最后
- 本skill当前处于初始阶段，遇到的漏洞类型还不算多，在我后续代审过程会不断更新、优化skill。
- 下载使用后，请不要完全依赖，希望你能对比源码和skil审计报告，找出skill漏报的漏洞类型，然后跟ai说：我发现audit-tracer未能发现xxx漏洞，请确认xxx漏洞是否存在，若存在则优化audit-tracer
- 如果你有空，希望你提一下，在使用过程中，有哪些漏洞类型漏洞，供大家优化自己的skill

