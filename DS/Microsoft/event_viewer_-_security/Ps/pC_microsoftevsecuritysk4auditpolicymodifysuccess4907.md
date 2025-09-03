#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-audit-policy-modify-success-4907
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """'EventID': 4907""", """'ObjectName': '""", """Auditing Settings Changed""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)\S*\s+[^\s]+\s+""",
    """EventID':\s+({event_code}\d+),""",
    """({event_name}Auditing Settings Changed)""",
    """SubjectUserName':\s+'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """SubjectDomainName':\s+'({domain}[^']+)'""",
    """SubjectUserSid':\s+('|")({user_sid}[^'"]+)('|")""",
    """SubjectIP':\s+'({src_ip}[a-dA-F\d:\.]+)'""",
    """ObjectServer':\s+'({object_server}[^']+)'""",
    """ObjectType':\s+'({object_type}[^']+)'""",
    """ObjectName':\s+'({object}[^']+)'""",
    """HandleID':\s+'({handle_id}[^']+)'""",
    """Computer':\s+[^\/]+\/({host}[^']+)'""",
    """Result':\s+'({action}[^']+)'"""
  ]
  DupFields = ["host->dest_host", "user->src_user", "domain->src_domain"]


}
```