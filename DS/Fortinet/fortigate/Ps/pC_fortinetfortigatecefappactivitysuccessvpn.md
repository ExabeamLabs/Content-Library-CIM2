#### Parser Content
```Java
{
Name = fortinet-fortigate-cef-app-activity-success-vpn
  ParserVersion = "v1.0.0"
  Conditions = [ """|Fortinet|Fortigate|""", """|event:vpn""", """FTNTFGTsubtype=vpn""" ]
  Fields = ${DLFortinetParsersTemplates.fortinet-network-info.Fields} [
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sspt=({src_port}\d+)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdpt=({dest_port}\d+)""",
    """\sout=({bytes_out}\d+)""",
    """\sin=({bytes_in}\d+)""",
    """\sact=({action}[^=]+?)\s\w+="""
  ]

fortinet-network-info = {
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "epoch_sec"
  Fields = [
    """FTNTFGTeventtime=({time}\d{10})""",
    """\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)""",
    """\|Fortinet\|Fortigate\|([^|]+\|){2}({event_name}[^|]+)\|""",
    """\smsg=({additional_info}[^"]+?)\s*(\w+=|$)"""
  
}
```