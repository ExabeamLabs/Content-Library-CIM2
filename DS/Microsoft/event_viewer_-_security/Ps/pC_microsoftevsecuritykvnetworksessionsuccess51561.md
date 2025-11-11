#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-network-session-success-5156-1"
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [ """ 5156 """, """篩選平台已經允許一個連線。""" ]
    Fields = [
      """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{3})""",
      """\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}[\-\+]\d\d:\d\d ({host}[\w.\-]+)\s""",
      """\d{2}:\d{2}:\d{2} ({dest_host}[\w.\-]+)\s""",
      """({event_code}5156)""",
      """處理程序識別碼:\s*({process_id}\d+)""",
      """應用程式名稱:\s*({process_path}({process_dir}(?:[^\^]+)?[\\\/]+)?({process_name}[^\\\/\^]+?))\s+網路資訊:""",
      """來源位址:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """來源連接埠:\s*({src_port}\d+)""",
      """目的地位址:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """目的地連接埠:\s*({dest_port}\d+)""",
      """通訊協定:\s*({protocol}\d+)""",
      """階層名稱:\s*({layer_name}[^\s]+)""",
      """方向:\s*({direction}輸入|輸出)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```