#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-access-5145-9
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Event Viewer - Security 
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [ """ 5145 """, """已檢查網路共用物件，查看是否可授與用戶端想要的存取權。""" ]
    Fields = [
      """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{3})""",
      """\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}[\-\+]\d\d:\d\d ({host}[\w.\-]+)\s""",
      """\d{2}:\d{2}:\d{2} ({dest_host}[\w.\-]+)\s""",
      """({event_code}5145)""",
      """\s安全性識別碼:\s*({user_sid}\S+)\s""",
      """\s帳戶名稱:\s*({user}[^\s]+)""",
      """\s帳戶網域:\s*({domain}[^\s]+)""",
      """\s登入識別碼:\s*({login_id}[^\s]+)""",
      """\s物件類型:\s*({file_type}[^\s]+)""",
      """\s來源位址:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\s來源連接埠:\s*({src_port}\d+)""",
      """\s共用名稱:\s*(?:\\\\\*\\)?({share_name}.+?)\s+共用路徑:""",
      """\s共用路徑:\s*(?:[\\\?]+)?(?:\s*|({share_path}(({d_parent}.+?)\\)?({d_name}\s*\S[^\\]+?))\\?\s+)相對目標名稱:""",
      """\s相對目標名稱:\s*\\?(?:\s*|(?:({file_dir}.+?)\\)?({file_name}[^\\:\/]+?(?:\.({file_ext}[^\.]+?))?)(?:\\HEAD|:.+?|\\|\s)\s*)存取要求資訊:""",
      """\s存取:\s*.*\s({access}SYNCHRONIZE|Execute|Traverse|Read|READ).*\s*存取檢查結果:""",
      """\s存取:\s*.*\s({access}WRITE_DAC|WRITE_OWNER|WriteAttributes|WriteEA).*\s*存取檢查
結果:""",
      """\s存取:\s*.*\s({access}WriteData|AppendData).*\s*存取檢查結果:""",
      """\s存取:\s*.*\s({access}delete|Delete).*\s*存取檢查結果:""",
      """\s存取檢查結果:\s*({result}-)\s""",
      """\s存取檢查結果:\s*.*({result}授與).*"""
    ]
  

}
```