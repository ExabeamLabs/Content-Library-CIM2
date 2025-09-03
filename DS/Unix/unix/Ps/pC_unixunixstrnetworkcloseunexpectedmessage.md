#### Parser Content
```Java
{
Name = unix-unix-str-network-close-unexpectedmessage
  Vendor = Unix
  Product = Unix
  TimeFormat = ["MMM dd yyyy HH:mm:ss.SSS","MMM dd HH:mm:ss"]
  Conditions = [ """%SSH""", """-SSH2_UNEXPECTED_MSG: """, """Unexpected message type has arrived""", """Terminating the connection from """ ]
  Fields = [
    """({time}\w+\s\d+\s\d\d:\d\d:\d\d)"""
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """({event_name}Terminating the connection)""",
    """Terminating the connection from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```