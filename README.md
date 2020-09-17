# LiveTV
Use Youtube live as IPTV feeds

## Install 

First you need to install Docker, Centos7 users can directly use the following tutorials. [How To Install and Use Docker on CentOS 7](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-centos-7)

After installing Docker, you can enable LiveTV! on your local port 9500 with the following command:

`docker run -d -p9500:9000 zjyl1994/livetv:1.0`

The data file is stored inside the container in the `/root/data` directory, so it is recommended to use the -v command to map this directory to the host's directory.

An example of using an external storage directory is shown below.

`docker run -d -p9500:9000 -v/mnt/data/livetv:/root/data zjyl1994/livetv:1.1`

This will open a LiveTV! container on port 9500 that uses the `/mnt/data/livetv` directory as storage.

PS: If you do not specify an external storage directory, LiveTV! will not be able to read the previous configuration file when it reboots.

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
