# nxcspray - NetExec (nxc) spraying
Simple bash script to spray known credentials against multiple services with NetExec (https://www.netexec.wiki/)

# Installation
Clone this repo or download the script directly.

Add the script to /usr/local/bin/ to execute it from anywhere on your machine, or use it in a local directory of your choice.
```
sudo mv ~/Downloads/nxcspray /usr/local/bin
chmod +x /usr/local/bin/nxcspray
```

# Usage
```
└─$ nxcspray -h, --help                 
[-] nxcspray <protocols|all> <targets> [auth] [spray-safety] [dump options] [-- <raw nxc args>]
```

Example Usage
```
nxcspray smb,winrm targets.txt -u e.hills -p 'Il0vemyj0b2025!'
```
<img width="1249" height="172" alt="image" src="https://github.com/user-attachments/assets/1d782a78-1e65-4483-8722-b602c1c1b774" />



```
nxcspray all 10.1.45.200 -u e.hills -p 'Il0vemyj0b2025!'
```
<img width="1315" height="365" alt="image" src="https://github.com/user-attachments/assets/65453924-98c5-44c1-975c-bfb40968ef88" />


```
nxcspray all hosts.txt -u users.txt -p 'Spring2026!' --continue-on-success --jitter 2-5
```

```
nxcspray smb 10.0.0.0/24 -u administrator -H aad3b...:31d6c... --local-auth --sam --lsa
```

```
nxcspray smb dc01.corp.local -u svc -p Pass1 -d corp.local -- -M ntdsutil
```
