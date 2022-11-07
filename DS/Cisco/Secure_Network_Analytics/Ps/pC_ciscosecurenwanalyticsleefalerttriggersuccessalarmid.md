#### Parser Content
```Java
{
Name = cisco-securenwanalytics-leef-alert-trigger-success-alarmid
  Vendor = Cisco
  Product = Secure Network Analytics
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """LEEF""", """StealthWatch[""", """|Lancope|Stealthwatch|""", """alarmID=""", """alarmSev=""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+StealthWatch\[""",
    """\Wstart=({time}\d+-\d+-\d+T\d+:\d+:\d+Z)""",
    """\Wsrc=(0.0.0.0|({src_ip}[A-Fa-f:\d.]+))""",
    """\Wdst=(0.0.0.0|({dest_ip}[A-Fa-f:\d.]+))""",
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