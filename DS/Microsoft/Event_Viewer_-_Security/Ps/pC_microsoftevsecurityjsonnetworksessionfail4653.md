#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-network-session-fail-4653
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """EventID":4653""", """An IPsec main mode negotiation failed""" ]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Hostname":"({host}[^"]+)"""",
    """"EventID":({event_code}4653)""",
    """({event_name}An IPsec main mode negotiation failed)""",
    """"LocalAddress":"({src_ip}[a-fA-F:\d.]+)"""",
    """"LocalKeyModPort":"({src_port}\d+)"""",
    """"RemoteAddress":"({dest_ip}[a-fA-F:\d.]+)"""",
    """"RemoteKeyModPort":"({dest_port}\d+)"""",
    """"FailureReason":"({failure_reason}[^"]+?)(\\r\\n)?"""",
# initiator_cookie is removed
# responder_cookie is removed
    """"EventType":"({action}[^"]+)""""
    ]


}
```