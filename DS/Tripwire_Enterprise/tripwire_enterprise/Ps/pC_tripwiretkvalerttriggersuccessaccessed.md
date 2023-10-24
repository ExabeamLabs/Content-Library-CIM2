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
   """LogUser="*(({domain}[^\\"]+?)\\+)?({user}[\w\.\-]{1,40}\$?)"*\s\w+?=""",
   """EventType=({access}[^\s=]+?)\s""",
   """AppType="*({app}[^=]+?)"*\s\w+?=""",
   """NodeIp=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
   """Msg='({src_file_path}({file_dir}[^'"]*?[\\\/]+)?({file_name}[^'"\\\/]+?(\.({src_file_ext}[^\d]+?))?))'\saccessed by"""
      ]


}
```