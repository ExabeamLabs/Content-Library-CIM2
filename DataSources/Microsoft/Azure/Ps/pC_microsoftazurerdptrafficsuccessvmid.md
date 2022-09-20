#### Parser Content
```Java
{
Name = microsoft-azure-rdp-traffic-success-vmid
  Vendor = Microsoft
  Product = Azure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""|beatname=eventhubbeat|""", """|device_type=eventhubbeat|""", """|subject=AdvancedHunting-DeviceEvents|""", """vmid=""", """@timestamp""", """@metadata""", """"ActionType":"RemoteDesktopConnection""""]
  Fields = [
    """@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """\d+-\d+-\d\dT\d+:\s\d+:\d+\.\d+\+\d+\s({host}[^\s]+)""",
    """subject=({event_name}[^|\s]+)""",
    """category":"({category}[^"]+)""",
    """ActionType":"({action}[^"]+)""",
    """DeviceName":"({dest_host}[^"]+)""",
    """sip=({src_ip}[A-Fa-f:\d.]+)""",
    """dip=({dest_ip}[A-Fa-f:\d.]+)""",
    """sport=({src_port}\d+)""",
    """dport=({dest_port}\d+)""",
    """protname=({protocol}[^|]+)""",
    """"RemoteUrl"+:"+({url}[^",]+)""",
    """domainorigin=({domain}[^|]+)""",
    """"InitiatingProcessId":({process_id}\d+)""",
    """"InitiatingProcessAccountName":"(system|SYSTEM|NETWORK SERVICE|local service|({user}[^"]+))""",
    """"InitiatingProcessAccountSid"+:"+({user_sid}[^"]+)""",
    """"LocalIP":"({src_ip}[A-Fa-f:\d.]+)""",
    """"LocalPort":({src_port}\d+)""",
    """"Protocol\\"+:\\"+({protocol}[^\\"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```