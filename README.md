# 在Windows下使用vscode实现lvgl仿真
实现方式基于lvgl仿真官方
[lv_sim_vscode_sdl](https://github.com/lvgl/lv_sim_vscode_sdl)
这个版本是在linux下实现的，我修改了Makefile文件让它能够在windows下能正常使用

主要就是修改环境设置，
```
	"tasks": [
		{
			"type": "shell",
			"label": "Build",
			"command": "mingw32-make",
			"options": {
				"cwd": "${workspaceFolder}"
			},
```
Makefile中重要的一点在于
```
shell find $(SRC_DIR) -type f -name "*.c" -not -path "*/\.*"
修改了原先的单引号''
```



ps:还有很多细节后续补充