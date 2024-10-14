#### Parser Content
```Java
{
Name = microsoft-azure-csv-rdp-traffic-success-vmid
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""|beatname=eventhubbeat|""", """|device_type=eventhubbeat|""", """|subject=AdvancedHunting-DeviceEvents|""", """vmid=""", """@timestamp""", """@metadata""", """"ActionType":"RemoteDesktopConnection""""]
  Fields = [
    """@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """\d+-\d+-\d\dT\d+:\s\d+:\d+\.\d+\+\d+\s({host}[^\s]+)""",
    """subject=({event_name}[^|\s]+)""",
    """category":"({category}[^"]+)""",
    """ActionType":"({result}[^"]+)""",
    """DeviceName":"({dest_host}[\w\-.]+)""",
    """sip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """sport=({src_port}\d+)""",
    """dport=({dest_port}\d+)""",
    """protname=({protocol}[^|]+)""",
    """"RemoteUrl"+:"+({url}[^",]+)""",
    """domainorigin=({domain}[^|]+)""",
    """"InitiatingProcessId":({process_id}\d+)""",
    """"InitiatingProcessAccountName":"(system|SYSTEM|NETWORK SERVICE|local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"InitiatingProcessAccountSid"+:"+({user_sid}[^"]+)""",
    """"LocalIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"LocalPort":({src_port}\d+)""",
    """"Protocol\\"+:\\"+({protocol}[^\\"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```