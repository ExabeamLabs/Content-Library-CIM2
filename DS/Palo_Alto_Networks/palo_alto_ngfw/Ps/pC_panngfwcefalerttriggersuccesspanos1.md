#### Parser Content
```Java
{
Name = pan-ngfw-cef-alert-trigger-success-panos-1
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "MMM dd yyyy HH:mm:ss zzz"
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Palo Alto Networks|PAN-OS|""", """|THREAT|""", """PanOSThreatCategory="""  ]
  Fields = [
    """\s({host}[\w\-.]+?)\sCEF:""",
    """\sdvchost=({host}[\w\-.]+)""",
    """\|rt=({time}\w\w\w\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d \w\w\w)""",
    """({alert_type}THREAT)""",
    """\scat=({alert_name}[^=]+)\s+\w+=""",
    """\|({alert_name}[^\|]+)\|THREAT\|({alert_severity}\d+)\|""", 
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\w+=""",	
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+\w+=""",
    """\sapp=({app}[^=]+)\s+\w+=""",
    """\sproto=({protocol}[^=]+?)\s+\w+=""",
    """\sact=({action}[^=]+?)\s+\w+=""",
    """\sspt=({src_port}\d+)""",
    """\sdpt=({dest_port}\d+)""",
    """\scs1="*({rule}[^="]+?)"*\s+\w+=""",
    """PanOSThreatCategory=({threat_category}[^=]+?)\s+\w+=""",
    """suser=(({domain}[^\\=]+?)\\+)?({user}[^\s=]+)\s+\w+=""",
    """\scs2=({category}[^=]+)\s+\w+=""",
    """\sflexString2=({direction}[^=]+)\s+\w+="""
  ]


}
```