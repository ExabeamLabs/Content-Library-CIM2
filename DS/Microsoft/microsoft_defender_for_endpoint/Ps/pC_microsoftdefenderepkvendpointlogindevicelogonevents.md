#### Parser Content
```Java
{
Name = microsoft-defenderep-kv-endpoint-login-devicelogonevents
  ParserVersion = "v1.0.0"
  Conditions = ["""|beatname=eventhubbeat|""", """|device_type=eventhubbeat|""", """|subject=AdvancedHunting-DeviceLogonEvents|""", """vmid=""", """@timestamp""", """@metadata""", """"ActionType":"""]
  Fields = ${DLMicrosoftParsersTemplates.azure-event-hub.Fields} [
    """"LogonType":"(Unknown|({login_type}\d+))""",
  ]

azure-event-hub = {
    Vendor = Microsoft
    Product = Microsoft Defender for Endpoint
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
       """@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
       """\d+-\d+-\d\dT\d+:\s\d+:\d+\.\d+\+\d+\s({host}[^\s]+)""",
       """category":"({category}[^"]+)""",
       """ActionType":"({event_name}[^"]+)""",
       """DeviceName":"({dest_host}[\w\-.]+)""",
       """"FileName":"({file_name}[^"]+)""",
       """"FolderPath":"({file_path}[^"]+)""",
       """"InitiatingProcessAccountDomain":"({domain}[^"]+)""",
       """"InitiatingProcessAccountName":"(system|local service|SYSTEM|NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
       """"InitiatingProcessAccountSid":"({user_sid}[^"]+)""",
       """"InitiatingProcessCommandLine":"\s*({process_command_line}.+?)\s*"+\,""",
       """"InitiatingProcessFileName":"({process_name}[^"]+)""",
       """"InitiatingProcessFolderPath":"({process_dir}[^"]+)""",
       """"InitiatingProcessParentFileName":"({parent_process_name}[^"]+)""",
       """"InitiatingProcessIntegrityLevel":"({process_integrity}[^"]+)""",
       """"MD5":"({hash_md5}[^"]+)""",
       """"InitiatingProcessId":({process_id}\d+)""",
       """"InitiatingProcessLogonId":({login_id}\d+)""",
    
}
```