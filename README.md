# LiveTV
Use Youtube live as IPTV feeds

## Install local
```
#git clone https://github.com/linsongze/livetv.git

#cd livetv 

#docker build . -f Dockerfile_Centos -t linsz/livetv

#docker run -d -p9500:9000  linsz/livetv

```


## Install kintohub
1、注册kintohub账号

2、创建免费的service,选择web app

3、import URL，输入本项目地址，connect

4、Port端口改成443

5、Dockerfile Name 改为 hintohub_Dockerfile

6、Deploy,等待结果，成功后，会在log窗口输出访问的路径



## Usage

Default password is "password".

First you need to know how to access your host from the outside, if you are using a VPS or a dedicated server, you can visit `http://your_ip:9500` and you should see the following screen.

![index_page](pic/index-en.png)

First of all, you need to click "Auto Fill" in the setting area, set the correct URL, then click "Save Config".

Then you can add a channel. After the channel is added successfully, you can play the M3U8 file from the address column.

When you use Kodi or similar player, you can consider using the M3U file URL in the first row to play, and a playlist containing all the channel information will be generated automatically.

Youtube-dl document here => [https://github.com/ytdl-org/youtube-dl](https://github.com/ytdl-org/youtube-dl)

Document Translate by [DeepL](https://www.deepl.com/zh/translator)
