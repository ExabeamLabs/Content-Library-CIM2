#### Parser Content
```Java
{
Name = "sybase-s-json-database-activity-success-accesstodb"
Conditions = [
"""object_name"""
""""event_desc""""
""""access to database""""
""""database_name""""
""""extra_info""""
]
ParserVersion = "v1.0.0"

f5-waf-activity-aa.Fields} [
    """\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\) CMD""",
    """\sCMD \(\s*({process_command_line}[^\)]+)\)""",
    """\sCMD \(\s*[^\/]*?({process_path}({process_dir}\/[^\)]*?)({process_name}[^\/]*?[^\\]))((\\\\)*\s|\))"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = huawei-usg-kv-process-create-success-shell
  Vendor = Huawei
  Product = Huawei Unified Security Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """SHELL/""", """ command=""", """ result=""" ]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
     """\sip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """\suser=(({email_address}[^@,]+@[^@,]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
     """\scommand=({process_command_line}({process_path}({process_dir}[^,]*?[\\\/]+)?({process_name}[^\\\/\s]+))[^,]*?),""",
     """\sresult=({result}\w+)""",
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = blackberry-protect-kv-alert-trigger-success-devicecontrol
  ParserVersion = v1.0.0
  Vendor = BlackBerry
  Product = BlackBerry Protect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """CylancePROTECT """, """Event Type: DeviceControl""", """Device Name:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})\d+""",
    """Event Type:\s*({alert_type}[^,]+)\s*,""",
    """Event Name:\s*({alert_name}[^,]+)\s*,""",
    """Device Name:\s*({src_host}[^,]+)\s*,""",
    """External Device Serial Number:\s*({device_id}[^,]+)\s*,""",
    """External Device Name:\s*({additional_info}[^,]+)\s*,""",
    """External Device Type:\s*({device_type}[^,]+)\s*,""",
  
}
```