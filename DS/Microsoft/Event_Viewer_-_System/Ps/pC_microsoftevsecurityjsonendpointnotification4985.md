#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-notification-4985
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - System
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = ["""The state of a transaction has changed""", """"EventID":4985"""]
  Fields = [
    """({event_name}The state of a transaction has changed)""",
    """({event_code}4985)""",
    """"EventTime":"({time}\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"Hostname":"({host}[^"]+)"""",
    """"SeverityValue":"({severity}[^,]+)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectUserName":"({user}[^"]+)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"LogonID":"({login_id}[^"]+)"""",
    """"TargetDomainName":"({group_domain}[^"]+)"""",
    """"ProcessId":"(\\t)*({process_id}[^\\]+)"""",
    """"ProcessName":"({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
# resource_manager is removed
    """"TransactionId":"({transaction_id}[^"]+)"""",
# new_state is removed

  ]
  DupFields = [ "host->dest_host" ]


}
```