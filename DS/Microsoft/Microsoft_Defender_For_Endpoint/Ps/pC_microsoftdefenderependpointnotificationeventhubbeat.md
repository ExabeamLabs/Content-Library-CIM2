#### Parser Content
```Java
{
Name = microsoft-defenderep-endpoint-notification-eventhubbeat
  ParserVersion = "v1.0.0"
  Conditions = ["""|beatname=eventhubbeat|""", """|device_type=eventhubbeat|""", """|subject=AdvancedHunting-DeviceInfo|""", """vmid=""", """@timestamp""", """@metadata"""]
  Fields = ${DLMicrosoftParsersTemplates.azure-event-hub-network-events.Fields} [
    """"MacAddress":"({src_mac}[^"]+)"""",
  ]

azure-event-hub-network-events = {
    Vendor = Microsoft
    Product = Microsoft Defender For Endpoint
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
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
    
}
```