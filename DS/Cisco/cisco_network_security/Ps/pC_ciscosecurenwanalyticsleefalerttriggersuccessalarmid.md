#### Parser Content
```Java
{
Name = cisco-securenwanalytics-leef-alert-trigger-success-alarmid
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """LEEF""", """StealthWatch[""", """|Lancope|Stealthwatch|""", """alarmID=""", """alarmSev=""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+StealthWatch\[""",
    """\Wstart=({time}\d+-\d+-\d+T\d+:\d+:\d+Z)""",
    """\Wsrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\Wdst=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\WdstPort=({dest_port}\d+)""",
    """\Wmsg=({alert_name}[^\|\=]+?)\.?\s*(\||$)""",
    """\Wcat=({alert_type}[^\|\=]+?)\.?\s*(\||$)""",
    """\WalarmID=({alert_id}[^\|\=]+?)\s*(\||$)""",
    """\WalarmSev=({alert_severity}[^\|\=\s]+?)\s*(\||$)""",
    """\Wdomain=({domain}[^\|\=\s]+?)\s*(\||$)""",
    """\Wfullmessage=({additional_info}[^\|]+?)\s*(\||$)"""
  ]
  ParserVersion = "v1.0.0"


}
```