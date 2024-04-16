#### Parser Content
```Java
{
Name = sophos-xgfirewall-kv-app-logout-success-loggedout
  Vendor = Sophos
  Product = Sophos XG Firewall
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
  Conditions = [ """device="SFW"""", """device_name="XG330"""", """log_component="GUI""", """logged out of Web Admin Console""" ]
  Fields = [
    """\Wdevice_name="({host}[^"]+)""",
    """\Wdate=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)""",
    """\Wstatus="({result}[^"]+)""",
    """\Wpriority=(|({alert_severity}.+?))(\s+\w+=|\s*$)""",
	"""\Wsrc_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\Wuser_name="(({email_address}[^\s@"]+@[^\s@"]+)|({user}[\w\.\-]{1,40}\$?))"""",
    """\Wlog_component="({app}GUI)"""",
    """\Wmessage="({additional_info}[^"]+)(\w+=|$|")""",
    """({event_name}logged out)"""
  ]


}
```