#### Parser Content
```Java
{
Name = cyberark-pam-kv-alert-trigger-success-attackblock
  Vendor = CyberArk
  Product = Cyberark Privilege Access Management
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CyberArk-EPM-Event {""", """'eventType': 'AttackBlock'""", """'sourceType':""" ]
  Fields = [
    """'arrivalTime':\s'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{0,3})?Z)'""",
    """'userName':\s'((\.|({domain}[^'\\]+))\\+)?({user}[^'\\]+)'""",
    """'eventType':\s'({alert_name}[^']+)'""",
    """'originalFileName':\s'({file_name}[^']+?(\.({file_ext}[^'\.]+))?)'""",
    """'filePath':\s'({file_path}[^']+)'""",
    """'fileSize':\s({bytes}\d+)""",
    """'commandLine':\s'({process_command_line}[^']+)'""",
    """'fileDescription':\s'({additional_info}[^']+)'""",
    """'displayName':\s'({additional_info}[^']+)'""",
    """'hash':\s'({file_hash}[^']+)'""",
    """'sourceWSName':\s'({src_host}[^']+)'"""
  ]
  DupFields = ["alert_name->alert_type"]
  ParserVersion = "v1.0.0"


}
```