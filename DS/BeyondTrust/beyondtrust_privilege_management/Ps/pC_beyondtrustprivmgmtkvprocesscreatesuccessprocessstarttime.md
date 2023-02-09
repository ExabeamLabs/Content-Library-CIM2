#### Parser Content
```Java
{
Name = beyondtrust-privmgmt-kv-process-create-success-processstarttime
  Vendor = BeyondTrust
  Product = BeyondTrust Privilege Management
  TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
  Conditions = [ """, ProcessStartTime="""", """, ProcessStartTimeMs="""" ]
  Fields = [
    """\WProcessStartTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\WHostName ="({host}[^"]+)""",
    """\WEventNumber="({event_code}\d+)""",
    """\WUserName ="(({domain}[^\\"]+)\\)?({user}[^\\"]+)""",
    """\WEventDescription="({additional_info}[^"]+)""",
    """\WFileName ="({process_path}({process_dir}(?:(\w+:)?[^:"]+)?[\\\/])?({process_name}.+?))"""",
    """\WCommandLine="({process_command_line}.+?)",""",
    """\WProductName ="(<None>|({product_name}[^"]+))""",
    """\WPublisher="(<None>|({publisher}[^"]+))""",
    """\WReason="(<None>|({failure_reason}[^"]+))""",
    """\WProcessGUID="({process_guid}[^"]+)""",
    """\WParentProcessUniqueID="({parent_process_guid}[^"]+)""",
    """\WPID="({process_id}[^"]+)""",
    """\WUserSID="({user_sid}[^"]+)""",
    """\WApplicationHash="({hash_md5}[^"]+)""",
    """\WActivityType="({operation_type}[^"]+)""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```