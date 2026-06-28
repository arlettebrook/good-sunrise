
## 🔑 变量说明

| 变量名 | 示例 | 必填 | 备注 | YT |
|--------|---------|-|-----|-----|
| UUID | `90cd4a77-141a-43c9-991b-08263cfe9c10` |✅| 可输入任意值(非UUIDv4标准的值会自动切换成动态UUID) | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=72s) |
| KEY | `token` |❌| 动态UUID秘钥，使用变量`KEY`的时候，将不再启用变量`UUID`|  |
| TIME | `7` |❌| 动态UUID有效时间(默认值:`7`天)|  |
| UPTIME | `3` |❌| 动态UUID更新时间(默认值:北京时间`3`点更新) |  |
| SCV | `false`或`0` |❌| 是否跳过TLS证书验证(默认`true`开启跳过证书验证) |  |
| PROXYIP | `proxyip.cmliussss.net:443` |❌| 备选作为访问CFCDN站点的代理节点(支持自定义ProxyIP端口, 支持多ProxyIP, ProxyIP之间使用`,`或`换行`作间隔) | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=166s) |
| HTTP  | `user:password@127.0.0.1:8080`或`127.0.0.1:8080` |❌| 优先作为访问CFCDN站点的HTTP代理(支持多HTTP代理之间使用`,`或`换行`作间隔) | |
| SOCKS5  | `user:password@127.0.0.1:1080`或`127.0.0.1:1080` |❌| 优先作为访问CFCDN站点的SOCKS5代理(支持多socks5, socks5之间使用`,`或`换行`作间隔) | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=826s) |
| GO2SOCKS5  | `blog.cmliussss.com`,`*.ip111.cn`,`*google.com` |❌| 设置`SOCKS5`或`HTTP`变量之后，可设置强制使用socks5访问名单(设置为`*`可作为全局代理) ||
| NAT64 | `dns64.cmi.ztvi.org`或`2001:67c:2960:6464::/96` |❌| 作为PROXYIP失效后的应急兜底，自行查询[nat64.xyz](https://nat64.xyz/)的`DNS64 Server`或`NAT64 Prefix` ||
| ADD | `icook.tw:2053#官方优选域名` |❌| 本地优选TLS域名/优选IP(支持多元素之间`,`或`换行`作间隔) ||
| ADDAPI | [https://raw.github.../addressesapi.txt](https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressesapi.txt) |❌| 优选IP的API地址(支持多元素之间`,`或 换行 作间隔) ||
| ADDNOTLS | `icook.hk:8080#官方优选域名` |❌| 本地优选noTLS域名/优选IP(支持多元素之间`,`或`换行`作间隔) ||
| ADDNOTLSAPI | [https://raw.github.../addressesapi.txt](https://raw.githubusercontent.com/cmliu/CFcdnVmess2sub/main/addressesapi.txt) |❌| 优选IP的API地址(支持多元素之间`,`或 换行 作间隔) ||
| ADDCSV | [https://raw.github.../addressescsv.csv](https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressescsv.csv) |❌| iptest测速结果(支持多元素, 元素之间使用`,`作间隔) ||
| DLS | `8` |❌| `ADDCSV`测速结果满足速度下限 ||
| CSVREMARK | `1` |❌| CSV备注所在列偏移量 ||
| TGTOKEN | `6894123456:XXXXXXXXXX0qExVsBPUhHDAbXXX` |❌| 发送TG通知的机器人token | 
| TGID | `6946912345` |❌| 接收TG通知的账户数字ID | 
| SUB | `SUB.cmliussss.net` | ❌ | 优选订阅生成器域名 | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1193s) |
| SUBAPI | `SUBAPI.cmliussss.net` |❌| clash、singbox等 订阅转换后端 | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1446s) |
| SUBCONFIG | [https://raw.github.../ACL4SSR_Online_Full_MultiMode.ini](https://raw.githubusercontent.com/cmliu/ACL4SSR/main/Clash/config/ACL4SSR_Online_Full_MultiMode.ini) |❌| clash、singbox等 订阅转换配置文件 | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1605s) |
| SUBEMOJI | `false` |❌| 订阅转换是否启用Emoji(默认`true`) | |
| SUBNAME | `edgetunnel` |❌| 订阅名称 | |
| RPROXYIP | `false` |❌| 设为 true 即可强制获取订阅器分配的ProxyIP(需订阅器支持)| [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1816s) |
| URL302 | `https://t.me/CMLiussss` |❌| 主页302跳转(支持多url, url之间使用`,`或`换行`作间隔, 小白别用) |  |
| URL | `https://blog.cmliussss.com` |❌| 主页反代伪装(支持多url, url之间使用`,`或`换行`作间隔, 乱设容易触发反诈) |  |
| CFPORTS | `2053`,`2096`,`8443` |❌| CF账户标准端口列表 |  |
| CF_EMAIL | `admin@google.com` |❌| CF账户的邮箱，用于获取 Workers/Pages 请求数 |  |
| CF_APIKEY | `1234567890abcdef1234567890abcdef` |❌| CF账户的`Global API Key`，用于获取 Workers/Pages 请求数 |  |

> **注意：** 只有 `CF_EMAIL` 和 `CF_APIKEY` 变量同时存在时，订阅时才会返回 CF Workers/Pages 的请求数用量信息。

## ❗ 注意事项

### 开启在线编辑优选列表 [视频教程](https://www.youtube.com/watch?v=tKe9xUuFODA&t=630s)
- 绑定**变量名称**为`KV`的**KV命名空间**，即可在无`SUB`的前提下，在配置页实现在线编辑`ADD`与`ADDAPI`优选列表；

### **关于`KEY`与`UUID`：**
- 填入`KEY`变量后，将停用`UUID`变量，请确保**二者选其一使用**！
1. 填写`KEY`后，您的**永久订阅**地址为：`https://[YOUR-URL]/[YOUR-KEY]`；
2. 使用动态`UUID`订阅时：
   - 动态`UUID`需手动在永久订阅配置页内获得；
   - 临时订阅地址为：`https://[YOUR-URL]/[动态UUID]`；
   - 订阅有效时间为：**1个`TIME`周期**；
   - 节点可使用时间：**2个`TIME`周期**，即动态`UUID`失效后，节点仍可使用1个额外周期，但无法继续更新订阅。

### **关于`SOCKS5`与`PROXYIP`：**
- 填入`SOCKS5`后，将停用`PROXYIP`。请确保**二者选其一使用**！

### **关于`SUB`与`ADD*`变量：**
- 填入`SUB`后，将停用由`ADD*`类变量生成的订阅内容。请确保**二者选其一使用**！

### **当`SUB`和`ADD*`均为空时：**
- 脚本将自动生成基于CF随机IP的线路，每次更新订阅时会生成不同的随机IP，确保您的订阅不会失联！


## 🔧 实用技巧
本项目提供灵活的订阅配置方案，支持通过URL参数快速自定义订阅内容。
- 示例订阅地址： `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` 

1. 更换**订阅生成器**的订阅地址 [视频教程](https://www.youtube.com/watch?v=tKe9xUuFODA&t=1019s)

   快速切换订阅生成器至 `VLESS.cmliussss.net`：
   ```url
   https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub=VLESS.cmliussss.net
   ```

2. 更换**PROXYIP**的订阅地址 [视频教程](https://www.youtube.com/watch?v=tKe9xUuFODA&t=1094s)

   快速更换PROXYIP为 `proxyip.cmliussss.net`：
   ```url
   https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?proxyip=proxyip.cmliussss.net
   ```

3. 更换**SOCKS5**的订阅地址

   快速设置SOCKS5代理为 `user:password@127.0.0.1:1080`：
   ```url
   https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?socks5=user:password@127.0.0.1:1080
   ```

- 通过提交多个参数快速修改的订阅地址

   例如同时修改**订阅生成器**和**PROXYIP**：
   ```url
   https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub=VLESS.cmliussss.net&proxyip=proxyip.cmliussss.net
   ```

4. 该项目部署的节点可通过节点PATH(路径)的方式，使用指定的`PROXYIP`或`SOCKS5`！！！**

- 指定 `PROXYIP` 案例
   ```url
   /proxyip=proxyip.cmliussss.net
   /?proxyip=proxyip.cmliussss.net
   /proxyip.cmliussss.net (仅限于域名开头为'proxyip.'的域名)
   ```

- 指定 `SOCKS5` 案例
   ```url
   /socks5=user:password@127.0.0.1:1080
   /?socks5=user:password@127.0.0.1:1080
   /socks://dXNlcjpwYXNzd29yZA==@127.0.0.1:1080 (默认激活全局SOCKS5)
   /socks5://user:password@127.0.0.1:1080 (默认激活全局SOCKS5)
   ```

- 指定 `HTTP代理` 案例
   ```url
   /http://user:password@127.0.0.1:8080 (默认激活全局SOCKS5)
   ```

5. **当你的`ADDAPI`可作为`PROXYIP`时，可在`ADDAPI`变量末位添加`?proxyip=true`，即可在生成节点时使用优选IP自身作为`PROXYIP`**
- 指定 `ADDAPI` 作为 `PROXYIP` 案例
   ```url
   https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressesapi.txt?proxyip=true
   ```

## ⭐ Star 星星走起
[![Stargazers over time](https://starchart.cc/cmliu/edgetunnel.svg?variant=adaptive)](https://starchart.cc/cmliu/edgetunnel)

## 💻 已适配客户端
### Windows
   - [v2rayN](https://github.com/2dust/v2rayN)
   - clash.meta（[FlClash](https://github.com/chen08209/FlClash)，[mihomo-party](https://github.com/mihomo-party-org/mihomo-party)，[clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev)，[Clash Nyanpasu](https://github.com/keiko233/clash-nyanpasu)）
### IOS
   - Surge，小火箭
   - sing-box（[SFI](https://sing-box.sagernet.org/zh/clients/apple/)）
### 安卓
   - clash.meta（[ClashMetaForAndroid](https://github.com/MetaCubeX/ClashMetaForAndroid)，[FlClash](https://github.com/chen08209/FlClash)）
   - sing-box（[SFA](https://github.com/SagerNet/sing-box)）
### MacOS
   - clash.meta（[FlClash](https://github.com/chen08209/FlClash)，[mihomo-party](https://github.com/mihomo-party-org/mihomo-party)）


# 🙏 特别鸣谢
### 💖 赞助支持 - 提供云服务器维持[订阅转换服务](https://sub.cmliussss.net/)
- [NodeLoc](https://www.nodeloc.com/)
- [Alice](https://url.cmliussss.com/alice)
- [EasyLinks](https://www.vmrack.net?ref_code=5Zk7eNhbgL7)
- [ZMTO(VTEXS)](https://zmto.com/?affid=1532)

### 🛠 开源代码引用
- [zizifn/edgetunnel](https://github.com/zizifn/edgetunnel)
- [3Kmfi6HP/EDtunnel](https://github.com/6Kmfi6HP/EDtunnel)
- [SHIJS1999/cloudflare-worker-vless-ip](https://github.com/SHIJS1999/cloudflare-worker-vless-ip)
- [Stanley-baby](https://github.com/Stanley-baby)
- [ACL4SSR](https://github.com/ACL4SSR/ACL4SSR/tree/master/Clash/config)
- [股神](https://t.me/CF_NAT/38889)
- [Workers/Pages Metrics](https://t.me/zhetengsha/3382)
- [白嫖哥](https://t.me/bestcfipas)