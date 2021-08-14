# dbird-behind

## How to use

### Shell
```sh
ssh -R $(d='' && read -p "Enter app name (default: ${d:-random}) : " v && echo ${v:-$d}):80:$(d='127.0.0.1' && read -p "Enter target hostname (default: $d) : " v && echo ${v:-$d}):$(d='80' && read -p "Enter target port (default: $d) : " v && echo ${v:-$d}) behind.dbird.ch
```

### PowerShell
```pwsh
ssh -R "$($d = ''; ($v = Read-Host ""Enter app name (default: $($d ? $d : 'random'))"") ? $v : $d):80:$($d = '127.0.0.1'; ($v = Read-Host ""Enter target hostname (default: $d)"") ? $v : $d):$($d = '80'; ($v = Read-Host ""Enter target port (default: $d)"") ? $v : $d)" behind.dbird.ch
```

### Manual
```sh
ssh -R <app name (optional)>:80:<target hostname (required)>:<target port (required)> behind.dbird.ch
```
