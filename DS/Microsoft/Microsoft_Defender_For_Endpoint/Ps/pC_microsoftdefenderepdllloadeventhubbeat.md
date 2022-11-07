#### Parser Content
```Java
{
Name = microsoft-defenderep-dll-load-eventhubbeat
    ParserVersion = "v1.0.0"
    Vendor = Microsoft
    Product = Microsoft Defender For Endpoint
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = ["""|beatname=eventhubbeat|""", """|device_type=eventhubbeat|""", """|subject=AdvancedHunting-DeviceImageLoadEvents|""", """vmid=""", """@timestamp""", """@metadata"""]
    Fields = [
      """time"+:\s*"+({time}[^"]+)"""",
      """category":"({category}[^"]+)""",
      """ActionType":"({event_name}[^"]+)""",
      """"DeviceName"+:\s*"+({dest_host}({host}[^"\.]+)?[^"]+)""",
      """"FileName":"+({file_name}[^"]+?(\.({file_ext}\w+))?)"""",
      """"FolderPath":"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
      """"InitiatingProcessAccountDomain":"({domain}[^"]+)""",
      """"InitiatingProcessAccountName":"(system|local service|SYSTEM|NETWORK SERVICE|({user}[^"]+))""",
      """"InitiatingProcessAccountSid":"({user_sid}[^"]+)""",
      """"InitiatingProcessCommandLine":"\s*({process_command_line}.+?)\s*"\,""",
      """"InitiatingProcessFileName":"({process_name}[^"]+)""",
      """"InitiatingProcessFolderPath":"+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?\.\w+?))"""",
      """"MD5":"({hash_md5}[^"]+)""",
      """"InitiatingProcessId":({process_id}\d+)""",
      """"InitiatingProcessLogonId":({login_id}\d+)""",
    ]


}
```