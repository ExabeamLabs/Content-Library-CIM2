#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-notification-4985
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ExtractionType = json
  Conditions = ["""The state of a transaction has changed""", """"EventID":4985"""]
  Fields = [
    """exa_json_path=$.Message,exa_regex=({event_name}The state of a transaction has changed)""",
    """exa_json_path=$.EventID,exa_field_name=event_code""",
    """exa_json_path=$..EventTime,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.Hostname,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$..SubjectUserSid,exa_field_name=user_sid""",
    """exa_json_path=$..SubjectUserName,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
    """exa_json_path=$..SubjectDomainName,exa_field_name=domain""",
    """exa_json_path=$.ProcessId,exa_field_name=process_id""",
    """exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$""",
    """exa_json_path=$..TransactionId,exa_field_name=transaction_id"""
  ]
  DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]


}
```