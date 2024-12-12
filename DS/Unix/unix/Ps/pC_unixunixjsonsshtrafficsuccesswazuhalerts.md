#### Parser Content
```Java
{
Name = "unix-unix-json-ssh-traffic-success-wazuhalerts"
Product = "Unix"
ExtractionType = json
Conditions = [
  """"decoder.parent":"sshd""""
  """Accepted """
  """ for """
  """ from """
  """"type":"wazuh-alerts""""
]
ParserVersion = "v1.0.0"


}
```