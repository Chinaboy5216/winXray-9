[winXray 入门小技巧](./sub/introduce.md)   
[winXray 相关视频列表](https://www.youtube.com/results?search_query=winXray)  
[网络免费 vmess 服务器订阅链接](https://proxypool.ga/vmess/sub)   
[网络免费 Shadowsocks 服务器订阅链接](https://proxypool.ga/ss/sub)     
[网络免费 clash 服务器订阅链接](https://proxypoolss.tk/clash/proxies?speed=100&type=vmess,trojan)   
可复制上面各种格式订阅链接，在 winXray 中点击「批量导入链接」体验 winXray 有强大的兼容性。  

# winXray 
winXray[:loud_sound:](http://dict.youdao.com/dictvoice?audio=winxray&type=2) 是最简洁轻快的 V2Ray、Trojan、Trojan-go、Shadowsocks、SSR(ShadowsocksR)、SSRoT 全能通用客户端（Windows系统），支持并发检测大量服务器并迅速找到当前最快的服务器，服务器连接异常时可自动寻找其他速度最快的服务器 - 切换速度快如闪电，自订阅源获取的服务器异常时可自动刷新订阅，并且自带一键自动部署服务端工具。

**本软件源码已放弃版权贡献到公共域** ，源码可使用 [aardio](http://www.aardio.com) 编译生成单文件绿色EXE，**[点这里下载](./../../raw/master/release/winXray.7z)** （ [64位版本](./../../raw/master/release/winXray.7z) / [32位版本](./../../raw/master/release/winXray32.7z) ），解压即可直接使用( 体积很小仅  **[6.1 MB](./../../raw/master/release/winXray.7z)** - 已自带 V2Ray Core ）。  

# 使用前必读    
最终都要删库跑路的原因大家都懂不用我多说了吧？！ 我删库特别快，是因为我写代码的速度快，我用了几小时就完成了 winXray 的主要代码，用了几天升级就迅速达到了一般其他软件写了几年的成熟度！因为我即将删库，但是我推上去的更新 - fork 的项目基本都没有那么迅速的主动拉更新，大家可以看一下 winXray 上线才短短几天就超过了 600 forks, 所以如果我推送更新之前不删库，那么我删库以后就没有人能找到最新版本的源代码。   
  
现在大多杀毒软件都是白名单查杀，所以新生的EXE都会乱报病毒，因为我更新的速度太快，所以不断的推新EXE上来，所以你可能遇到误报，但是你完全可以使用源代码自己编译出一模一样的EXE，还有人吹牛说其他翻墙软件不误报 - 你去 issues 里以及网上搜一下有多少误报好不好？！遇到误报可以提交给你的杀毒厂商核实，也可以自己编译源码生成EXE后使用，解决和核实问题很容易 - 其他套路都是多余的。
  
本来 winXray 源码已放弃版权贡献到公共域，但是有人把源码拿去拖了个又大又丑的推广按钮上去，什么功能也不加就发布新版自称官方，而且还把源码搞得很乱出了问题的对本作者进行诋毁（ 错误信息都看不懂居然自称开源软件官方 ），对提及原版 winXray 的帖子进行封删和威胁，我真是惊到了世上居然有如此无耻之人，本来就是给你自由发挥的，吃相这么难看良心不会痛吗？！本来我想改一个许可证限制一下这种不好的行为，但是最后我还是决定继续放弃版权，继续将源码贡献到公共域，即然开放源码，就一定要开放得彻底，我们不能因为世上有个别的恶棍而放弃自己善良的初心。 

# 关于 PAC 代理：
winXray 的 PAC 代理稳定、流畅、易用。  在 PAC 模式下，winXray 会优先启用高效安全的 SOCKS5 协议，并且可以自动兼容在 PAC 模式下仅支持 HTTP代理的应用。winXray 也可以在 PAC 模式下完美支持 Telegram IP 地址库（ 旧版本升级请在 PAC 编辑器右键添加 Telegram IP 地址库 ） 。

PAC 属于系统代理规则 - 是一种非常成( 老 )熟( 了 )的代理模式，与翻墙软件完全无关并完全独立，可以保证只有需要经过代理的域名才与翻墙软件发生关系。PAC 主要支持浏览器，可以避免迅雷、百度网盘、Steam 等流量在未经许可时经过翻墙软件。也只有 PAC 能真正让浏览器直接支持高效安全的 SOCKS5 协议，否则就只能改为低版本 SOCKS 或者 HTTP 代理。启用 PAC 也并不会影响大家使用 V2Ray Core 自带的路由规则 -  实际上在 winXray 中使用自带的路由规则是非常方便的( winXray 在配置界面可直接修改 Core 配置 )。 

# 设置系统代理失败怎么办
如果设置代理以后不能正常生效：请首先右键点击 winXray 任务栏的托盘图标，在弹出的右键菜单中点击【查看 Internet 代理设置】，并检查代理设置是否正常。如果 winXray 不能修改代理设置，但是可以手动修改成功，这一般是被安全软件错误地拦截了( 而且安全软件没有正常弹出确认对话框，或者误点了阻止设置 ）。这时候请到安全软件的相关设置中将 winXray 添加到信任列表即可。

如果不是上面的原因，请按下【Win + R】组合键打开系统运行对话框，输入 regedit 点击确定打开注册表路径 
<span style="color:green">HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Internet Settings\Connections</span>
然后将“Connections”项删除，注销一下系统即可正常使用代理了。

如果上面的方法仍然不行，请在注册表中打开打开路径
<span style="color:green">Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\WinHttpAutoProxySvc</span>
将 start 的值改为 2， 也就是将 WinHttpAutoProxySvc 服务改为自动启动，然后重启计算机即可。

# 关于 V2Ray Core / SSR Core 默认路径：

默认会在以下目录查找 V2Ray Core：

    ./v2ray-core/
    %localappdata%\winXray\core

默认会在以下目录查找 SSR Core：

    ./v2ray-core/ssr-core
    %localappdata%\winXray\ssr-core

找不到会自动下载，没有代理访问 Github 会很慢很慢，有时可能根本打不开，建议经常运行一下 winXray 工具里自带的 【Github 网速优化工具】