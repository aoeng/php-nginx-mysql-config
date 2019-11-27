- 导入box:`matdata.json`

```
{
	"name": "laravel/homestead",
	"versions": [{
		"version": "8.2.1",
		"providers": [{
			"name": "virtualbox",
			"url": "file:///D:/Work/Boxs/homestead-8.2.1.box"
		}]
	}]
}
```

- 设置全局:`homestead.bat`

```
@echo off

set cwd=%cd%
set homesteadVagrant=D:\Work\Homestead

cd /d %homesteadVagrant% && vagrant %*
cd /d %cwd%

set cwd=
set homesteadVagrant=

```

- 开机启动:`autostart.bat`

``` 
set ws=WScript.CreateObject("WScript.Shell")
ws.Run "homestead up",0
```
`win+R` 输入`shell:startup`

创建快捷方式放入其中