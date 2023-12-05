#### Parser Content
```Java
{
Name = symantec-bcpa-str-network-traffic-fail-ssl
  ParserVersion = v1.0.0
  Conditions = [
"""PROXIED""",
"""- ssl"""
  ]
  DupFields =["http_response_code->result_code"]


}
```