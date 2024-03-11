#### Parser Content
```Java
{
Name = cisco-c-mix-endpoint-logout-success-sessionexited
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """-LOGOUT: """, """has exited tty session""" ]
  Fields = [
    """<\d+>[^:\s]+:\s+({host}[^:\s]+):""",
    """({event_code}\S+\d+-LOGOUT):""",
    """User\s*({user}\S+)\s+has exited tty session""",
    """\(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?)\)\s*$""",
  ] 


}
```