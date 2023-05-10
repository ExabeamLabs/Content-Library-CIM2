#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-4985-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss+SS:SS"
  Conditions = [ """Event_ID="4985"""", """The state of a transaction has changed""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\+\d+:\d+)\s({host}[^\s]+)""",
    """Event_ID="+({event_code}\d+)""",
    """sourceip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """({event_name}The state of a transaction has changed)""",
    """Subject:\s+Security ID:\s+({user_sid}[^\s]+)""",
    """SubjectUserName ="+({user}[^"]+)"""
    """SubjectDomainName ="+({domain}[^"]+)""",
    """SubjectLogonId="+({login_id}[^"]+)""",
# transcation_id is removed
# new_state is removed
# resource_manager is removed
    """ProcessId="+({process_id}[^"]+)""",
    """ProcessName ="+({process_path}({process_dir}[^.]+)\\({process_name}[^"]+))""",
    """Computer="+({host}[^"]+)"""
  ]
   DupFields = [ "host-> dest_host" ]


}
```