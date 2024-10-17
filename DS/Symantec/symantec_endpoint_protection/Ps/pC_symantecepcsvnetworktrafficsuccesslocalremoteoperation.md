#### Parser Content
```Java
{
Name = symantec-ep-csv-network-traffic-success-localremoteoperation
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Conditions = [ """本地:""", """远程:""", """规则:""", """操作:""" ]
  Fields = [
    """\W开始:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d((\+|\-)\d\d:\d\d)?)""",
    """({host}[\w\-\.]+)\s*SymantecServer:""",
    """,本地:\s*({src_ip}[a-fA-F:\.\d]+),本地:\s*({src_port}\d+),本地:\s*({src_host}[\w\-\.]+),""",
    """,远程:\s*({dest_ip}[a-fA-F:\.\d]+),远程:\s*(|({dest_host}[\w\-\.]+)),远程:\s*({dest_port}\d+),""",
    """({protocol}[^,]+),({direction}[^,]+),开始:""",
    """\W应用程序:\s*({process_path}.*[\\\/]({process_name}[^\\\/,]+))""",
    """\W规则:\s*({event_name}[^,]+)""",
    """\W操作:\s*({action}[^,]+?)"*\s*$""",
    """\W用户:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?),域:\s*({domain}[^,]+)"""
  ]


}
```