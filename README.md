# MC-BOT
白嫖群黑白作品

## 环境变量

| 变量 | 必填 | 默认 | 说明 |
|---|---|---|---|
| `PANEL_PASS` | 是 | 无 | 面板登录密码，未设置则拒绝启动 |
| `PANEL_USER` | 否 | `admin` | 面板登录用户名 |
| `SERVER_PORT` | 否 | `4681` | 监听端口（Dockerfile 中设为 `7860`） |

面板使用 HTTP Basic Auth 保护，全部页面与 `/api/*` 接口都需要认证。浏览器访问时会弹出
登录框，输入上面配置的用户名与密码即可。密码按 realm 缓存在浏览器会话中，刷新页面不会
重复弹出；如需登出，关闭浏览器即可。

部署示例：

```bash
PANEL_USER=admin PANEL_PASS=你的密码 npm start
```
