#### Parser Content
```Java
{
Name = cisco-securenwanalytics-cef-alert-trigger-success-fcdvc
  Vendor = Cisco
  Product = Secure Network Analytics
  TimeFormat =  "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CEF:""", """cisco|stealthwatch""", """category=""", """fc_dvc_ip=""", """fc_dvc=""" ]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d+-\d+T\d+:\d+:\d+\.\d+Z)""",
    """fc_dvc=({host}[^\s]+)""",
    """CEF:([^\|]+\|){2}({alert_name}[^\|]+)""",
    """CEF:([^\|]+\|){5}({event_name}[^\|]+)""",
    """CEF:([^\|]+\|){6}({alert_severity}[^\|]+)""",
    """category=({alert_type}[^=]+?)\s+\w+=""",
    """message=({additional_info}[^=]+)\s+\w+=""",
    """src_ip=({src_ip}[a-fA-F\d:\.]+)""",
    """dest_ip=(0\.0\.0\.0|({dest_ip}[a-fA-F\d:\.]+))""",
    """src=({src_host}[^\s]+)""",
    """src_user=({user}[^\s]+)""",
    """dest=({dest_host}[^\s]+)""",
    """dest_port=({dest_port}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```