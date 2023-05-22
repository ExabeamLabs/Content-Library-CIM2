#### Parser Content
```Java
{
Name = pan-ngfw-cef-alert-trigger-success-spyware
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "MMM dd yyyy HH:mm:ss zzz"
  Conditions = [ """CEF""", """|Palo Alto Networks|PAN-OS|""", """|THREAT|""", """cat=spyware"""  ]
  Fields = [
    """\sdvchost=({host}[\w\-.]+)""",
    """\|rt=({time}\w\w\w\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d \w\w\w)""",
    """({alert_type}spyware)""",
    """\scat=({alert_name}[^=]+)\s+(\w+=|$)""",
    """Palo Alto Networks\|PAN-OS\|[^\|]+\|({alert_name}[^(:]+)(\s*[^\|]+)\|""",
    """Palo Alto Networks\|PAN-OS\|([^\|]+\|){3}({alert_severity}\d)\|rt=""",
    """\sshost=({src_host}[^=]+)\s+(\w+=|$)""",
    """\sdhost=({dest_host}[^=]+)\s+(\w+=|$)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(\w+=|$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+(\w+=|$)""",
    """\seventId=({alert_id}\d+)\s+(\w+=|$)""",
    """\sapp=({threat_category}[^=]+)\s+(\w+=|$)""",
    """\sproto=({protocol}[^=]+?)\s+\w+=""",
    """\sact=({action}[^=]+?)\s+\w+=""",
    """\sspt=({src_port}\d+)""",
    """\sdpt=({dest_port}\d+)""",
    """\scs1="*({rule}[^="]+?)"*\s+\w+="""
    """\sapp=({app}[^=]+)\s+\w+=""",
    """\scs2=({category}[^=]+)\s+\w+=""",
    """\sflexString2=({direction}[^=]+)\s+\w+="""
  ]
  ParserVersion = v1.0.0


}
```