请认真看完本文章,再提出你的疑问,如果文章对你有帮助,麻烦点个关注支持UP！

Q:"videoconfig.txt"文件在哪儿？有什么注意事项？
A:首先是步骤
SETP.1 "Win+R"或者WIN10搜索框输入:%USERPROFILE%\Saved Games\Respawn\Apex\local
		（找到:C:\Users\你的用户名\Saved Games\Respawn\Apex\local中的Videoconfig）
SETP.2 打开"Videoconfig.txt"清空你的内容。
		复制UP放在下面的CFG替换。

Q:有什么注意事项?
A:改完保存，右键属性改为只读并应用。

Q:为什么要改成只读?
A:如果不改成只读,你在游戏中有任何画质的改动，都会将CFG重置成默认（指重置阴影/额外修改的数值），并且注释翻译会被自动清除。所以一定要改成只读。

数字对应的等级均为UP本人进行过验证，不要再问为什么是3为什么是2而不是-9999了。

诸如 我的显卡是XX型号,怎么调比较好 , 下面我会直接推荐一些方案给你 ，节省时间成本。

授人鱼，不如授之以渔。UP并不靠这些吃饭。无偿分享自己知道的东西。

关于方案推荐；如果你觉得我的方案多余/认为我为什么要这么麻烦写方案.请直接绕道关掉我的文章，这里只提供给有需要的人自取，谢谢配合。
.纹理方案:
.A方案：
	"setting.stream_memory"		"160000"	//纹理串流预算
	"setting.mat_picmip"		"1"			//贴图清晰度
（可以看清楚皮肤,符合大多数人的设置）

.B方案：
	"setting.stream_memory"		"300000"	//纹理串流预算
	"setting.mat_picmip"		"0"	//贴图清晰度
比A方案高一个等级的清晰度,但是一般不是细看的情况是看不出区别的,还是A方案适合大多数人。

.C方案：
	"setting.stream_memory"		"0"	//纹理串流预算
	"setting.mat_picmip"		"2"	//贴图清晰度
	黄金游戏体验。
    
.纹理过滤方案:
.A方案：
	"setting.mat_forceaniso"	"1"			//纹理过滤等级	双线性:"1"/三线性:"1"/各向异性过滤:"2"/"4"/"8"/"16"
	"setting.mat_mip_linear"	"0"			//线性过滤开关		双线性:"0"/三线性-16x各向异性:"1.0"
        （"最低等级"的过滤设置,推荐对远处物体表面清晰度不敏感的玩家使用）
        
.B方案：
	"setting.mat_forceaniso"	"4"			//纹理过滤等级	双线性:"1"/三线性:"1"/各向异性过滤:"2"/"4"/"8"/"16"
	"setting.mat_mip_linear"	"1"			//线性过滤开关		双线性:"0"/三线性-16x各向异性:"1.0"
        （4X各向异性过滤是“性价比”最好的一个值,对清晰度有一定要求的推荐使用）

.TSAA抗锯齿:
	"setting.mat_antialias_mode"				"0"			//TSAA抗锯齿		禁用:"0"/开:"12"
        (抗锯齿,推荐分辨率1080P以下（不含1080）关闭,1080P(含)及以上自行决定开关)
   
分辨率方案:
标准方案:
	"setting.defaultres"						"1920"		//水平分辨率-w
	"setting.defaultresheight"					"1080"			//垂直分辨率-h
	"setting.fullscreen"						"1"			//全屏			禁用:"0"/开:"1.0"
	最基础的分辨率,不用UP多说了吧.

最有效"大幅度提升帧数"的方案:
标准方案:
	"setting.defaultres"						"1280"		//水平分辨率-w
	"setting.defaultresheight"					"960"			//垂直分辨率-h
	"setting.fullscreen"						"1"			//全屏			禁用:"0"/开:"1.0"
	自己习惯一下上下黑边,up主目前用的就是这个,帧数基本稳定170以上。（1070）习惯了和1080没区别。反而因为全屏拉伸，视觉感受更流畅。

其它设置,如"垂直同步,特效，布娃娃，阴影"等对帧数没有提升的"杂项"，UP的建议是都关闭和拉到最低。下面的"完整VIDEOCFG"照抄就可以。需要改的方案这里也都有。

顺带一提"自适应分辨率功能"虽然可以稳定和提升帧数,但是牺牲了太多的画质，就之前我发的视频中大家的反响得出的结论，显卡的锐化功能带来的视觉效果远不如直接降低分辨率的“性价比”高，所以推荐"不要开启"，帧生成时间越小画质越差但画面延迟会相对降低一些（在硬件基础上）。
Videocfg.txt完整内容

"VideoConfig"
{
	"setting.cl_gib_allow"					"0"			//布娃娃系统		禁用:"0"/开:"1.0"
	"setting.cl_particle_fallback_base"			"3"			//粒子基础			低(关):"3"/中:"0.00"/高:"0"
	"setting.cl_particle_fallback_multiplier"		"2"			//粒子倍增器		低(关):"2"/中:"1.75"/高:"1"
	"setting.cl_ragdoll_maxcount"				"0"			//布娃娃系统		低:"0"/中:"4"/高:"8"
	"setting.cl_ragdoll_self_collision"			"0"			//布娃娃碰撞		禁用:"0"/开:"1.0"
	"setting.mat_forceaniso"					"1"			//纹理过滤等级		双线性:"1"/三线性:"1"/各向异性过滤:"2"/"4"/"8"/"16"
	"setting.mat_mip_linear"					"0"			//线性过滤开关		双线性:"0"/三线性-16x各向异性:"1.0"
	"setting.stream_memory"					"160000"		//纹理串流预算 		建议:"0":4-6GVRAM(无)/"16w":6GVRAM(很低)/"30w":6.5GVRAM(低)/"60w":7GVRAM(中)/"100w":8GVRAM(高)/"200w":10GVRAM(很高)/"300w":10+GVRAM(超高)
 	"setting.mat_picmip"						"1"			//纹理贴图清晰度		糊:"2"/标清:"1"/高清:"0"
	"setting.particle_cpu_level"				"0"			//特效细节			低:"0"/中:"1.0"/高:"2.0"
	"setting.r_createmodeldecals"				"0"			//冲撞痕迹贴图等级	禁用:"0"/低:"0.0"/高:"1.0"
	"setting.r_decals"						"0"			//冲撞痕迹			禁用:"0"/低:"256"/高:"256"
	"setting.r_lod_switch_scale"				"0.6"			//模型细节刷新		低:"0.35-0.6"中:"0.8"高:"1.0"(低于0.6若卡顿/看不清远处模型,设置回0.6就行)
	"setting.shadow_enable"					"0"			//阴影(点光源)		禁用:"0"/开:"1.0"
	"setting.shadow_depth_dimen_min"			"0"			//点光源阴影细节min	禁用:"0"/低:"128"/高:"256"/非常高:"512"
	"setting.shadow_depth_upres_factor_max"		"0"			//点光源阴影细节max	禁用:"0"/低:"2.0"/高:"2.0"/非常高:"3.0"
	"setting.shadow_maxdynamic"				"0"			//动态点光源阴影		禁用:"0"/开:"4.0"
	"setting.ssao_enabled"					"0"			//环境光遮蔽 		禁用:"0"/开:"1.0"
	"setting.ssao_downsample"					"3"			//环境光等级 		禁用:"3"/低:"2"/中:"1"/高:"0"
	"setting.dvs_enable"						"0"			//自适应分辨率帧率目标	禁用:"0"/开:"1.0"（配合自适应超级采样"1"使用）
	"setting.dvs_gpuframetime_min"				"0"			//最小帧生成时间		默认:"15000"(120FPS:"7949" - "8200" 144FPS: "6592" - "6800" 183FPS: "5250" - "5350" 200FPS: "4750" - "4900")
	"setting.dvs_gpuframetime_max"				"0"			//最大帧生成时间		默认:"16500"(120FPS:"7949" - "8200" 144FPS: "6592" - "6800" 183FPS: "5250" - "5350" 200FPS: "4750" - "4900")
	"setting.defaultres"						"1920"		//水平分辨率-w
	"setting.defaultresheight"					"1080"			//垂直分辨率-h
	"setting.fullscreen"						"1"			//全屏			禁用:"0"/开:"1.0"
	"setting.nowindowborder"					"0"			//无边框			禁用:"0"/开:"1.0"
	"setting.volumetric_lighting"				"0"			//体积光			禁用:"0"/开:"1.0"
	"setting.mat_vsync_mode"					"0"			//垂直同步模式		禁用:"0"/双缓冲  :"1"/三重缓冲  :"2"/自适应  :"3"/自适应半刷新率  :"4"-(FPS不能稳定屏幕刷新率不建议开启垂直同步,可能会造成输入滞后)
	"setting.mat_backbuffer_count"				"0"			//垂直同步缓冲		禁用:"1"/双缓冲时:"1"/三重缓冲时:"2"/自适应时:"1"/自适应半刷新率时:"1"-(FPS不能稳定屏幕刷新率不建议开启垂直同步,可能会造成输入滞后)
	"setting.mat_antialias_mode"				"0"			//TSAA抗锯齿		禁用:"0"/开:"12"
	"setting.csm_enabled"						"0"			//阴影			禁用:"0"/开:"1.0"
	"setting.csm_coverage"					"0"			//阳光阴影范围		禁用:"0"/低:"1.0"/高:"2.00"
	"setting.csm_cascade_res"					"0"			//阳光阴影细节		禁用:"0"/低:"512"/高:"1024"
	"setting.fadeDistScale"					"1.000000"		//体积渲染距离		默认:"1"/可尝试:"0.75"
	"setting.dvs_supersample_enable"			"0"			//自适应超级采样		(需要同时开启TSAA抗锯齿√自适应分辨率帧率目标√)
	"setting.gamma"							"1.000000"		//亮度(gamma)		50%:"1"/55%:"0.935714"/60%:"0.855357"/100%:"0.250000"
	"setting.configversion"					"7"			//Config版本		7
}
文件内容翻译及对照校准:桐生Kiryuz

以上设置内容"在游戏中的设定":
""""""""""""""""""""""""""""""""""
TSAA抗锯齿:"关"
纹理串流预算:"非常低"(皮肤很清楚)
纹理过滤:"双线性"
环境光遮蔽质量:"禁用"
阳光阴影范围:"低"
阳光阴影细节:"低"
点光源阴影细节:"禁用"
体积光:"禁用"
动态点光源阴影:"禁用"
模型细节:"低"
特效细节:"低"
冲撞痕迹:"禁用"
布娃娃系统:"关"

启动项使用方法:"steam"-"游戏库"右键单击"APEX Legends"-"属性"-"通用"-"启动选项"
关于启动项UP并没有推荐的，请各位玩家自行取舍，启动项也没有好与坏,只有你需不需要.
up自用的启动项：
-high -dev -fullscreen -freq 189 -refresh 189 +fps_max 189 +miles_language English -console -dxlevel95 -preload +mat_compressedtextures 1 +reticle_color "-50 200 400"

启动项说明（任何设置都是基于硬件层面的，要想真正的提升，还是要升级硬件，仅供参考！）:
-high:游戏高优先级
-dev:跳过启动时的开场动画
-fullscreen:全屏
-freq 240:设定屏幕刷新率，后面的数字填你的屏幕刷新率(不是帧数)
+miles_language english:英语语音。
-console:启动控制台(游戏里看不见,没什么实际作用,纯个人习惯)
-dxlevel95:DX9提高性能？UP没有真正的测试过,反正添加了没有看到负面影响。
-preload:预载资源,提高帧率，具体不知道提升多少,添加了也没见负面影响。
+fps_max 0:设置限制最大帧数限制,最好是再N卡里单独限制。
+mat_compressedtextures 1:压缩纹理,提高帧数?可能有提升。
+reticle_color "-50 200 400":准星颜色青色
-freq 240/189/144/120:基于你的显示器刷新率来设置。
-refresh 240/189/144/120:同上,二选一随便用。
其它可用的指令:
-fullscreen:让游戏以全屏独占模式启动
-w 1920 -h 1080:启动项设置分辨率
-windowed:让游戏以窗口模式启动，和-noborder一起使用来以无边框全屏模式启动
-noborder:让游戏以无边框模式启动，和-window一起使用来以无边框窗口模式启动游戏
+shownet_enabled "1":显示高级网络参数
+cl_showfps "1"/"2"/"4":显示高级FPS参数124决定显示位置
+cl_showpos "1":在左上角显示玩家名称、位置、速度信息
+miles_channels "2":强制使用立体声(双声道)   
+gfx_nvnUseLowLatency "1":启动项控制低延迟模式
+exec autoexec:运行自定义cfg，类似CSGO的CFG，但我们玩到的APEX不能呼出控制台只能在启动项中使用）   
cl_forcepreload "1":用于禁止"纹理/材质"预载到内存(类似-preload)，让其随地图同时加载，缺点是加载纹理的时间较长，相比cl_forcepreload "0"，cl_forcepreload "1"有更稳定的"帧速率"("frame time")或更短的"帧生成时间"，如果发生卡顿，只需删除此条即可。
🔥开启电源卓越性能代码。

使用"Windows PowerShell"创建"卓越性能模式"电源计划
"卓越性能模式"代码:
"powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61"
如何创建"卓越性能模式"电源管理计划:

方法1：通过"Win+X"菜单打开
	按"Win+X"快捷键（或右键点击Win10开始按钮）弹出系统快捷菜单，即可看到"Windows PowerShell"和"Windows PowerShell创建(管理员)"选项，点击即可打开。

方法2:Cortana搜索
	在任务栏中的"Cortana搜索框"中输入"PowerShell"，即可搜索到"Windows PowerShell"桌面应用，点击即可打开，右键"管理员运行"。

方法3：运行命令打开
	"Win+R"快捷键调出"运行"对话框，输入"PowerShell"，确定，即可打开"Windows PowerShell"。
     
    
如何打开"电源计划"控制面板，方法如下：
    "Win+R" 快捷键调出“运行”对话框，输入"rundll32.exe shell32.dll,Control_RunDLL powercfg.cpl"，确定，即可打开"电源计划"
关闭 XBOX DVR （windows游戏高光时刻自动录制）

方法一:windows设置中关闭,不会自行百度。

方法二:桌面新建一个文本,粘贴下面内容进去保存,并修改文件后缀为disableDVR.reg

查看文件后缀方法自行百度。
