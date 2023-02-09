#### Parser Content
```Java
{
Name = tripwire-t-kv-alert-trigger-success-accessed
  ParserVersion = v1.0.0
  Vendor = Tripwire Enterprise
  Product = Tripwire Enterprise
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ TE: """, """LogUser=""" , """EventType=""", """ accessed by """  ]
  Fields = [
   """HostName =({host}[\w.-]+?)\s""",
   """LogUser="*(({domain}[^\\"]+?)\\+)?({user}[^\s="]+?)"*\s\w+?=""",
   """EventType=({access}[^\s=]+?)\s""",
   """AppType="*({app}[^=]+?)"*\s\w+?=""",
   """NodeIp=({src_ip}[A-Fa-f\d.:]+?)\s""",
   """Msg='({src_file_path}({file_dir}[^'"]*?[\\\/]+)?({file_name}[^'"\\\/]+?(\.({src_file_ext}[^\d]+?))?))'\saccessed by"""
      ]


}
```