#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-windows"
Conditions = [
""""data.id":"4776""""
""""type":"wazuh-alerts""""
""""decoder.parent":"windows""""
]
DupFields = [
  "result_code->failure_code",
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```