
netsh interface ipv4 show global

netsh int ipv4 set glob defaultcurhoplimit=65
netsh int ipv6 set glob defaultcurhoplimit=65

netsh int ipv4 set glob defaultcurhoplimit=128
netsh int ipv6 set glob defaultcurhoplimit=128



HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters
DWORD (32-bit), DefaultTTL, 41 (16進位) = 65 (十進位)


https://github.com/RiFi2k/unlimited-tethering
https://wiki.termux.com/wiki/Remote_Access

termux

  pkg update && pkg install openssh
  pkg install termux-services

  passwd
  
  ifconfig
  whoami

  ssh-keygen -A
  
  sshd -hD
  pkill sshd
  
pc
  adb forward tcp:8022 tcp:8022

  ssh-keygen -t rsa

  #ssh-keygen -t rsa -b 2048 -f id_rsa
  #ssh-copy-id -p 8022 -i id_rsa IP_ADDR
  
  scp -P 8022 "D:\platform-tools\sshkey_20250720.pub" u0_260@localhost:~/.ssh/

  ssh -p 8022 u0_260@10.150.32.46

  ssh -D 1080 -p 8022 u0_260@10.150.32.46

 & "C:\Program Files\Google\Chrome\Application\chrome.exe" --proxy-server="socks5://127.0.0.1:1080" --host-resolver-rules="MAP * ~NOTFOUND , EXCLUDE 127.0.0.1"
 
 
 