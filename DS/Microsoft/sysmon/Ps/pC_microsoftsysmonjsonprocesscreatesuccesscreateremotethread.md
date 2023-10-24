#### Parser Content
```Java
{
Name = "microsoft-sysmon-json-process-create-success-createremotethread"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Microsoft-Windows-Sysmon""",
"""CreateRemoteThread detected:""",
""""TargetImage":""""
]
Fields = [
    """"UtcTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """"(Source)?Image":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """"TargetFilename":"({dest_process}(({dest_process_dir}[^"]*?)[\\\/]+)?({dest_process_name}[^"\\\/]+?(\.({dest_process_ext}\w+))?))"""",
    """"Domain":"(NT AUTHORITY|({domain}[^"]+))""",
    """"AccountName":"(SYSTEM|({user}[\w\.\-]{1,40}\$?))""",
    """"SourceProcessId":"({process_id}\d+)""",
    """"SourceProcessGuid":"({process_guid}[^"]+)""",
    """"TargetProcessId":"({dest_process_id}\d+)""",
    """"TargetProcessGuid":"({dest_process_id}[^"]+)""",
    """"LogonId":"({login_id}[^"]+)""",
    """"Hostname":"({host}[^"]+)""",
    """"TargetImage":"({dest_process}(({dest_process_dir}[^"]*?)[\\\/]+)?({dest_process_name}[^"\\\/]+))"""",
    """"EventID":({event_code}\d+)""",
    """"SourceImage":"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """"Category":"({event_name}[^"]+)""",
]
DupFields = [  "host->src_host", "dest_process->dest_process_path" ]
ParserVersion = "v1.0.0"


}
```