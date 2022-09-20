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
    """process=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""", """fileName =(|%FILENAME%|({src_file_path}({src_file_dir}[^=]+?)(\\({src_file_name}[^\\]+(\.({src_file_ext}[\w~]+))))?))\s+newFileName =""",
    """newFileName =(|({file_path}({file_dir}[^=]+?)(\\({file_name}[^\\]+(\.({file_ext}[\w]+))))?))\s+process="""
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```