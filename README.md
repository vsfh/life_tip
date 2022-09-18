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
sudo mount -t cifs -o dir_mode=0777,file_mode=0777 //192.168.22.17/share /mnt/share
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
