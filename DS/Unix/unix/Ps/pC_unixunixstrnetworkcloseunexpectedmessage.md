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
    """Terminating the connection from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```