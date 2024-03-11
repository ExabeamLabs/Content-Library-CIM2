#### Parser Content
```Java
{
Name = stealthbits-ssd-cef-alert-trigger-abnormaluserbehavior
  ParserVersion = v1.0.0
  Vendor = StealthBits
  Product = StealthBits Stealth Defend
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Conditions = [ """CEF:""", """|STEALTHbits Technologies|StealthDEFEND|""", """threatType=Abnormal User Behavior """]
  Fields = [
    """threatTime=({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\dZ)""",
    """computers=([^\\]+\\)?({host}[^;]+)""",
    """threatType=({alert_name}[^=]+)\s+\w+=""",
    """users=(({domain}[^\\]+)\\)?({user}[^\s;]+)""",
    """process=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""", """fileName =(|%FILENAME%|({src_file_path}({src_file_dir}[^=]+?)(\\({src_file_name}[^\\]+(\.({src_file_ext}[\w~]+))))?))\s+newFileName =""",
    """newFileName =(|({file_path}({file_dir}[^=]+?)(\\({file_name}[^\\]+(\.({file_ext}[\w]+))))?))\s+process="""
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```