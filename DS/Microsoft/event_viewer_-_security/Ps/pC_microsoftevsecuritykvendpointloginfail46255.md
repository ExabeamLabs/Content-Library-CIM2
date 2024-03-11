#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-fail-4625-5
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    ParserVersion = "v1.0.0"
    Conditions = [ """ 4625 """, """帳戶無法登入。""" ]
    Fields = [
      """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{3})""",
      """\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}[\-\+]\d\d:\d\d ({host}[\w.\-]+)\s""",
      """\d{2}:\d{2}:\d{2} ({dest_host}[\w.\-]+)\s""",
      """({event_code}4625)""",
      """帳戶無法登入。.+?帳戶名稱:\s*(?:-|({src_user}.+?))\s+帳戶網域:""",
      """帳戶無法登入。.+?帳戶網域:\s*(?:-|({src_domain}.+?))\s+登入識別碼:""",
      """登入類型:\s+({login_type}\d+)""",
      """登入失敗的帳戶:\s+安全性識別碼:\s+({user_sid}[^\s]+)\s+帳戶名稱:""",
      """登入失敗的帳戶:.+?帳戶名稱:\s+(?=\w)({user}.+?)\s+帳戶網域:""",
      """登入失敗的帳戶:.+?帳戶網域:\s+(?=\w)({domain}.+?)\s+失敗資訊:""",
      """失敗原因:\s*({failure_reason}.+?)\s+狀態:""",
      """子狀態:\s+({result_code}[^\s]+)\s""",
      """來源網路位址:\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """來源連接埠:\s*({src_port}\d+)""",
      """登入處理程序:\s+({auth_process}[^\s]+)\s+驗證封裝:\s+({auth_package}[^\s]+)"""
    ]
  

}
```