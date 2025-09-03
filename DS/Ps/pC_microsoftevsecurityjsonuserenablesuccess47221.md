#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-enable-success-4722-1
Conditions = [
  """"event_id":4722"""
  """Microsoft-Windows-Security-Auditing"""
  """A user account was enabled"""
]
ExtractionType = json
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```