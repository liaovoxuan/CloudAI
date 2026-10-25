# CloudAI 隐私政策 / Privacy Policy / 隱私政策

最后更新 / Last updated / 最後更新：2026-09-19

## 简体中文

### 适用范围

CloudAI 是客户端应用，可以连接用户选择并配置的 AI 服务。应用并非完全离线运行；请在发送机密内容前阅读相应服务商的隐私政策、数据保留规则和账户设置。

### 数据处理与网络连接

- 对话请求可能向所选 AI 服务商发送提示词、对话内容、附件、API 凭据以及处理请求所需的技术元数据。
- 查询余额时，应用可能访问该服务商的账户或用量接口。
- 使用 Agent 网页搜索时，搜索词会发送至 DuckDuckGo；打开外部网址时，系统浏览器会连接对应站点。
- Agent 模式可能读取用户纳入任务范围的文件或命令输出，并在确认后执行写文件、运行命令、打开网址或插件操作。
- 第三方插件在本地以应用进程的权限运行，并可能采用其自身的数据处理方式。请只安装可信插件。

上述第三方可能收到 IP 地址等常规网络元数据，并依据各自政策处理收到的数据。CloudAI 项目无法控制第三方的数据处理行为。

### 本地数据与凭据

配置、聊天记录、导出内容和日志可能存放在本地。CloudAI 1.0.1 会在界面中掩码显示 API Key，但磁盘文件仅使用可逆混淆，并非系统级加密；能够读取该文件的人可能恢复密钥。请保护本地文件与备份，不要共享 API Key，并及时撤销可能泄露的凭据。

日志、截图和问题报告可能包含提示词、路径或系统信息；公开提交前请先脱敏。删除本地数据不会自动删除第三方服务商已经接收或保留的数据。

### 用户控制

仅在了解操作范围后启用 Agent 或插件，并在敏感或破坏性操作前仔细检查确认提示。用户可以删除本地配置和聊天记录、卸载应用，并在服务商处撤销 API Key。安全敏感问题请按仓库中的 `SECURITY.md` 私下报告。

## English

### Scope

CloudAI is a client application that can communicate with AI services selected and configured by the user. It is not a completely offline application. Review the selected provider's privacy policy, retention rules and account settings before sending confidential information.

### Data processing and network connections

- Chat requests may send prompts, conversation content, attachments, API credentials and technical request metadata to the selected AI provider.
- Balance checks may contact account or usage endpoints operated by that provider.
- When Agent web search is used, the search query is sent to DuckDuckGo. Opening an external URL connects to that destination through the system browser.
- Agent mode may read files or command output placed within the task's scope and, after confirmation, write files, run commands, open URLs or invoke plugins.
- Third-party plugins run locally with the permissions of the application process and may have their own data practices. Install only plugins you trust.

Those third parties may receive ordinary network metadata such as the user's IP address and process received data under their own policies. The CloudAI project does not control third-party data handling.

### Local data and credentials

Configuration, chat history, exports and logs may be stored locally. CloudAI 1.0.1 masks API keys in the interface, but the on-disk file uses reversible obfuscation rather than operating-system-backed encryption. Anyone who can read that file may be able to recover the key. Protect local files and backups, do not share API keys, and revoke any credential that may have been exposed.

Logs, screenshots and issue reports may contain prompts, paths or system details; redact them before posting publicly. Deleting local data does not automatically delete data already received or retained by a third-party provider.

### User control

Enable Agent mode or plugins only after reviewing their scope, and inspect confirmation prompts before sensitive or destructive actions. Users can delete local configuration and chat history, uninstall the application, and revoke API keys with their providers. Report security-sensitive issues privately as described in the repository's `SECURITY.md`.

## 繁體中文

### 適用範圍

CloudAI 是用戶端應用程式，可以連線至使用者選擇並設定的 AI 服務。應用程式並非完全離線運作；傳送機密內容前，請先閱讀相應服務商的隱私權政策、資料保留規則及帳戶設定。

### 資料處理與網路連線

- 對話請求可能向所選 AI 服務商傳送提示詞、對話內容、附件、API 憑證及處理請求所需的技術中繼資料。
- 查詢餘額時，應用程式可能連線至該服務商的帳戶或用量介面。
- 使用 Agent 網頁搜尋時，搜尋詞會傳送至 DuckDuckGo；開啟外部網址時，系統瀏覽器會連線至相應網站。
- Agent 模式可能讀取使用者納入工作範圍的檔案或命令輸出，並在確認後寫入檔案、執行命令、開啟網址或呼叫外掛程式。
- 第三方外掛程式會在本機以應用程式處理程序的權限執行，並可能採用其自身的資料處理方式。請只安裝可信任的外掛程式。

上述第三方可能收到 IP 位址等一般網路中繼資料，並依各自政策處理收到的資料。CloudAI 專案無法控制第三方的資料處理行為。

### 本機資料與憑證

設定、聊天記錄、匯出內容及日誌可能儲存在本機。CloudAI 1.0.1 會在介面中遮罩顯示 API Key，但磁碟檔案僅使用可逆混淆，並非作業系統層級加密；能夠讀取該檔案的人可能還原金鑰。請保護本機檔案及備份，不要分享 API Key，並及時撤銷可能已洩漏的憑證。

日誌、螢幕截圖和問題回報可能包含提示詞、路徑或系統資訊；公開提交前請先去識別化。刪除本機資料不會自動刪除第三方服務商已接收或保留的資料。

### 使用者控制

只有在了解操作範圍後才啟用 Agent 模式或外掛程式，並在敏感或破壞性操作前仔細檢查確認提示。使用者可以刪除本機設定和聊天記錄、解除安裝應用程式，並在服務商處撤銷 API Key。安全敏感問題請依照倉庫中的 `SECURITY.md` 私下回報。
