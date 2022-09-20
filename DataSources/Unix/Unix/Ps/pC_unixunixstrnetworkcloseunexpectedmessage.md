#### Parser Content
```Java
{
Name = unix-unix-str-network-close-unexpectedmessage
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%SSH""", """-SSH2_UNEXPECTED_MSG: """, """Unexpected message type has arrived""", """Terminating the connection from """ ]
  Fields = [
    """({event_name}Terminating the connection)""",
    """Terminating the connection from ({src_ip}[a-fA-F\d:.]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```