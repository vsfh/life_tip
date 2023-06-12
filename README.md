# life_tip

## openwrt router v2ray

```
https://www.wyr.me/post/619
http://loonlog.com/2020/3/13/v2ray-for-openwrt-config/
```

## pull remote branch

```
git init
git remote add origin git@...
git fetch origin branch_name
git checkout -b local_branch_name origin/branch_name
git pull origin branch_name
```

## proxychains 

```
https://github.com/rofl0r/proxychains-ng
socks5 192.168.2.89 1089
https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt
```

## finalshell

```
adduser username not useradd
sudo usermod -aG sudo username
```

## softlink

```
sudo mount -t cifs -o uid=1000,file_mode=0777,dir_mode=0777 //192.168.2.217/share /mnt/share
```

## Gitpod

```
n62wrnyf
```
## cuda

```
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-ubuntu2004.pin
sudo mv cuda-ubuntu2004.pin /etc/apt/preferences.d/cuda-repository-pin-600
sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/3bf863cc.pub
sudo add-apt-repository "deb https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/ /"
sudo apt-get update
sudo apt-get -y install cuda
```

## delete

```
find ./stylegan3_r_2538 -type f -delete
export CUDA_HOME=/usr/local/cuda-11
```

## create new branch

```
git checkout -b my-test  //在当前分支下创建my-test的本地分支分支
git push origin my-test  //将my-test分支推送到远程
git branch --set-upstream-to=origin/my-test //将本地分支my-test关联到远程分支my-test上   
git branch -a //查看远程分支 
```

## set wsl proxy in bashrc

```
#获取宿主机的IP
export windows_host=`ipconfig.exe | grep -n4 WSL | tail -n 1 | awk -F":" '{ print $2 }' | sed 's/^[ \r\n\t]*//;s/[ \r\n\t]*$//'`

#假设宿主机代理端口是7890
export ALL_PROXY=http://$windows_host:7890
export HTTP_PROXY=$ALL_PROXY
export http_proxy=$ALL_PROXY
export HTTPS_PROXY=$ALL_PROXY
export https_proxy=$ALL_PROXY

#设置git的代理
if [ "`git config --global --get https.proxy`" != "http://$windows_host:7890" ]; then
	git config --global https.proxy http://$windows_host:7890
fi

if [ "`git config --global --get http.proxy`" != "http://$windows_host:7890" ]; then
	git config --global http.proxy http://$windows_host:7890
fi
```

