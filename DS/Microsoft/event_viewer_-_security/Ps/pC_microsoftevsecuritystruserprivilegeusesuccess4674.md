#### Parser Content
```Java
{
Name = "microsoft-evsecurity-str-user-privilege-use-success-4674"
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat  =  ["yyyy-MM-dd HH:mm:ss", "MM/dd/yyyy hh:mm:ss a", "MMM dd HH:mm:ss"]
  Conditions  =  [  """4674""",  """特権のあるオブジェクトで操作が試行されました。""",  """特権:"""]
  Fields  =  [
   """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)""",
   """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),""",
   """({dest_host}({host}[\w.\-]+))[,\]]\s*特権のあるオブジェクトで操作が試行されました。""",
   """\sID:\s*({login_id}[^\s]+?)\s+アカウント名:\s*({user}(SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON)|([\w\.\-\!\#\^\~]{1,40}\$?))\s*アカウント\s+ドメイン:\s*({domain}((NT AUTHORITY)|[^\s]+?))\s+ログオン""",
   """アカウント名:\s*({user}(SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON)|([\w\.\-\!\#\^\~]{1,40}\$?))\s*アカウント\s+ドメイン:\s*({domain}((NT AUTHORITY)|[^\s]+?))\s+ログオン\s*ID:\s*({login_id}[^\s]+?)\s+オブジェクト:""",
   """オブジェクト サーバー:\s*({object_server}.*?)\s*オブジェクトの種類:\s*(?:-|({object_type}.*?))\s*オブジェクト名:\s*(?:-|({object}.*?))\s*オブジェクト ハンドル:""",
   """プロセス名:\s+({process_path}({process_dir}.*?\\)({process_name}[^\\]*?))\s+要求された操作:""",
   """望ましいアクセス権:\s*({access}.*?)\s*特権:\s*({privileges}.*?)\s*($|"|,)"""
   """({event_code}4674)""",
   """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(AM|PM))"""
  ]


}
```