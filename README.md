<img width="1481" height="104" alt="image" src="https://github.com/user-attachments/assets/b6d95b64-3ba4-405a-a414-6bdbd595ca4d" /># hw2
HCI第二次作业：大语言模型部署与应用实践 以 —— DeepSeek 为例

## 1. API 调用与基础交互
### 1.1 API KEY设置
#### 1.1.1 deepseek
  deepseek的API注册入口非常好找，于是我先注册后寻找下一步，但是发现DeepSeek并没有免费额度。
  <img width="2128" height="1109" alt="image" src="https://github.com/user-attachments/assets/3c3d64ff-1618-42a5-a5e4-fbc22b3cd867" />
  于是转攻——
#### 1.1.2 ModelScope
  ModelScope的API注册入口相对来说有一点不好找（因为没有把“API”字样放在明面上），但是也很顺利地找到了我的API。
  <img width="1852" height="617" alt="image" src="https://github.com/user-attachments/assets/b4957b52-1273-4ec3-83d1-c6a81c6fa14e" />
  （它在这里的名字叫访问令牌）
### 1.2 程序与实现
  python代码可以通过PyCharm编辑，也可以直接用记事本编辑。
  <img width="1643" height="1267" alt="image" src="https://github.com/user-attachments/assets/3fc171fa-c796-44e6-8718-0bf153e75d42" />

  保存后通过cmd窗口运行。
  <img width="1350" height="1348" alt="image" src="https://github.com/user-attachments/assets/8a25b9b3-a181-449f-b2d9-7813ecf680ad" />

## 2. 本地部署与模型量化
### 2.1 使用Google Colab T4 配置环境
  1. 打开Google Colab，更改运行时类型为T4，保存。
     <img width="913" height="821" alt="image" src="https://github.com/user-attachments/assets/3ca90f8b-ba74-41ab-a83e-e72414773f20" />
     <img width="1183" height="1145" alt="image" src="https://github.com/user-attachments/assets/36d70c96-1912-4696-9b76-a607cb55f9ae" />

  2. 输入如图代码，安装环境。
  <img width="1456" height="510" alt="image" src="https://github.com/user-attachments/assets/7d8a695e-10df-4967-aa0a-dc7d9bd6578e" />
  <img width="1447" height="900" alt="image" src="https://github.com/user-attachments/assets/97b8749a-e84e-43a0-bc7f-6b00cb69f4c6" />

### 2.2 开始测试
#### 2.2.1 测试量化前数据

   <img width="1215" height="810" alt="image" src="https://github.com/user-attachments/assets/17a45309-eab7-4ef8-94ba-0052c984a184" />
  量化前显存占用为3549MiB /  15360MiB
  原始模型耗时: 3.21 秒

#### 2.2.2 测试量化后数据

  ![Uploading image.png…]()
  可以看到量化前显存占用为3613MiB /  15360MiB
  量化模型耗时: 3.25 秒


