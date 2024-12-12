#### Parser Content
```Java
{
Name = "unix-unix-json-endpoint-login-fail-authfailures"
Product = "Unix"
ExtractionType = json
Conditions = [
  """"decoder.name":"sshd""""
  """Too many authentication failures for"""
  """"type":"wazuh-alerts""""
]
ParserVersion = "v1.0.0"


}
```