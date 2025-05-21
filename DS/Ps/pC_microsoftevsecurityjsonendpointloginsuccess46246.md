#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-success-4624-6"
Conditions = [
  """subject.logon_id"""
  """"EventID""""
  """"4624""""
  """An account was successfully logged on"""
]
ExtractionType = json
DupFields = [ "src_host_windows->src_host", "host->dest_host" ]
ParserVersion = "v1.0.0"


}
```