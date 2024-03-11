#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-handle-request-4656
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"EventID":4656,""", """A handle to an object was requested""" ]
  Fields = [
    """({event_name}A handle to an object was requested)""",
    """({event_code}4656)""",
    """"EventTime"+:\s*"+({time}[^",]+)""",
    """"Hostname"+:"+({host}[^",]+)""",
    """"SubjectUserSid"+:"+({user_sid}[^",]+)"""",
    """"SubjectUserName"+:"+({user}[^",]+)"""",
    """"SubjectDomainName"+:"+({domain}[^",]+)"""",
    """"SubjectLogonId"+:"+({login_id}[^",]+)"""",
    """"TransactionId"+:"+({transaction_id}[^",]+)"""",
    """Accesses:(?:\s|\\t|\\r|\\n)*({access}[^:]+?)(?:\s|\\t|\\r|\\n)*Access Reasons:""",
    """"AccessReason"+:"+(-|({access}[^",]+))""",
    """"PrivilegeList"+:"+(-|({privileges}[^",]+))""",
    """({operation_type}requested)""",
    """"ProcessID"+:"+({process_id}[^",]+)"""",
    """"ProcessName"+:"+({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
    """"ObjectType"+:"+(Unknown|({object_type}[^",]+))"""",
    """"ObjectName"+:"+(Unknown|({object}[^",]+))"""",
    """"ObjectServer"+:"+({object_server}[^",]+)"""",
    """"HandleId"+:"+({object_id}[^",]+)"""",
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""
  ]
  DupFields = [ "host->dest_host", "access->privileges" ]


}
```