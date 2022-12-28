#### Parser Content
```Java
{
Name = cyberark-epm-json-user-privilege-use-success-elevationrequest
  ParserVersion = v1.0.0
  Vendor = CyberArk
  Product = Cyberark Endpoint Protection Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CyberArk-EPM-Event {""", """'eventType': 'ElevationRequest'""", """'sourceType':""" ]
  Fields = [
    """'arrivalTime':\s'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{0,3})?Z)'""",
    """'userName':\s'((\.|({domain}[^'\\]+))\\+)?({user}[^'\\]+)'""",
    """'eventType':\s'({event_name}[^']+)'""",
    """'originalFileName':\s'({file_name}[^']+?(\.({file_ext}[^'\.]+))?)'""",
    """'filePath':\s'({file_path}[^']+)'""",
    """'fileSize':\s({bytes}\d+)""",
    """'commandLine':\s'({process_command_line}[^']+)'""",
    """'fileDescription':\s'({additional_info}[^']+)'""",
    """'displayName':\s'({additional_info}[^']+)'"""
  ]
  DupFields = [ "event_name->operation" ]


}
```