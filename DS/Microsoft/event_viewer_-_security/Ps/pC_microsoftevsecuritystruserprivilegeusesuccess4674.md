#### Parser Content
```Java
{
Name = "microsoft-evsecurity-str-user-privilege-use-success-4674"
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat  =  "yyyy-MM-dd HH:mm:ss"
  Conditions  =  [  """4674""",  """特権のあるオブジェクトで操作が試行されました。""",  """特権:"""]
  Fields  =  [
   """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),""",
   """({host}[\w.\-]+),特権のあるオブジェクトで操作が試行されました。""",
   """アカウント名:\s*({user}.*?)\s*アカウント  ドメイン:\s*({domain}.*?)\s*ログオン  ID:\s*({login_id}.*?)\s*オブジェクト:""",
   """オブジェクト サーバー:\s*({object_server}.*?)\s*オブジェクトの種類:\s*(?:-|({object_type}.*?))\s*オブジェクト名:\s*(?:-|({object}.*?))\s*オブジェクト ハンドル:""",
   """プロセス名:\s+({process_path}({process_dir}.*?\\)({process_name}[^\\]*?))\s+要求された操作:""",
   """望ましいアクセス権:\s*({access}.*?)\s*特権:\s*({privileges}.*?)\s*($|"|,)"""
   """({event_code}4674),"""
  ]
  DupFields  =  [  "host->dest_host" ]


}
```