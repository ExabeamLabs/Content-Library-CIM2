#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-handle-request-4659
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = ["""A handle to an object was requested with intent to delete""", """4659""", """Microsoft-Windows-Security-Auditing"""]
  Fields = [
    """({event_name}A handle to an object was requested with intent to delete)""",
    """({event_code}4659)""",
    """rt=({time}\d+)""",
    """dvchost=({host}.*?)\s\w+="""
    """dhost=({dest_host}.*?)\s\w+="""
    """eventId=({event_code}.*?)\s\w+=""",
    """externalId=({external_id}.*?)\s\w+=""",
    """categoryBehavior=//?({action}.*?)\s\w+=""",
    """categoryOutcome=//?({result}.*?)\s\w+=""",
    """categoryObject=//?({object}.*?)\s\w+=""",
    """dst=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """dntdom=({domain}.*?)\s\w+=""",
    """duser=({user}.*?)\s\w+=""",
    """duid=({user_uid}.*?)\s\w+=""",
    """fname=({file_path}.*?)\s\w+=""",
    """fileType=({file_type}.*?)\s\w+=""",
    """ahost=({src_host}.*?)\s\w+="""
    """agt=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """amac=({src_mac}.*?)\s\w+=""",
# privilege_list is removed
    """TransactionId=\s*\{({transaction_id}[^\}]+)""",
    """ProcessID=({process_id}\d+)""",
  ]


}
```