#### Parser Content
```Java
{
Name = microsoft-defenderep-scheduled_task-create-scheduledtaskcreated
  ParserVersion = "v1.0.0"
  Conditions = ["""|beatname=eventhubbeat|""", """|device_type=eventhubbeat|""", """|subject=AdvancedHunting-DeviceEvents|""", """vmid=""", """@timestamp""", """@metadata""", """"ActionType":"ScheduledTaskCreated""""]
  Fields = ${DLMicrosoftParsersTemplates.azure-event-hub.Fields} [
    """\\"+TaskName\\"+:\\"+({task_name}[^"]+)""",
  ]

azure-event-hub = {
    Vendor = Microsoft
    Product = Microsoft Defender For Endpoint
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
       """@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
       """\d+-\d+-\d\dT\d+:\s\d+:\d+\.\d+\+\d+\s({host}[^\s]+)""",
       """category":"({category}[^"]+)""",
       """ActionType":"({event_name}[^"]+)""",
       """DeviceName":"({dest_host}[^"]+)""",
       """"FileName":"({file_name}[^"]+)""",
       """"FolderPath":"({file_path}[^"]+)""",
       """"InitiatingProcessAccountDomain":"({domain}[^"]+)""",
       """"InitiatingProcessAccountName":"(system|local service|SYSTEM|NETWORK SERVICE|({user}[^"]+))""",
       """"InitiatingProcessAccountSid":"({user_sid}[^"]+)""",
       """"InitiatingProcessCommandLine":"\s*({process_command_line}.+?)\s*"+\,""",
       """"InitiatingProcessFileName":"({process_name}[^"]+)""",
       """"InitiatingProcessFolderPath":"({process_dir}[^"]+)""",
       """"InitiatingProcessParentFileName":"({parent_process}[^"]+)""",
       """"InitiatingProcessIntegrityLevel":"({process_integrity}[^"]+)""",
       """"MD5":"({hash_md5}[^"]+)""",
       """"InitiatingProcessId":({process_id}\d+)""",
       """"InitiatingProcessLogonId":({login_id}\d+)""",
    
}
```