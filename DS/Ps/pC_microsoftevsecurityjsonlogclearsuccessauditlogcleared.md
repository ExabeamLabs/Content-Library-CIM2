#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-log-clear-success-auditlogcleared
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """EventCode=1102"""
  """The audit log was cleared"""
]
DupFields = [ "host->dest_host" ]
ParserVersion = "v1.0.0"


}
```