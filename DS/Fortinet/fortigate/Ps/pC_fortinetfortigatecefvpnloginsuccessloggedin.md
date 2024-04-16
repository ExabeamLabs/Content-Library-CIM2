#### Parser Content
```Java
{
Name = fortinet-fortigate-cef-vpn-login-success-loggedin
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "epoch"
  Conditions = [ """|Fortinet|Fortigate|""", """|event:vpn success|""", """FTNTFGTeventtime=""", """FTNTFGTsubtype=vpn""" ]
  Fields = [
    """FTNTFGTeventtime=({time}\d{13})""",
    """\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sspt=({src_port}\d{1,5})""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdpt=({dest_port}\d{1,5})""",
    """\sact=({action}[^=]+?)\s\w+=""",
    """FTNTFGTresult=({result}[^"]+)$""",
    """\|Fortinet\|Fortigate\|([^|]+\|){2}({event_name}[^|]+)\|""",
    """FTNTFGTdir=({direction}[^=]+?)\s\w+=""",
    """\smsg=({additional_info}[^=]+?)\s\w+=""",
    """outcome=({result}[^=]+?)\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```