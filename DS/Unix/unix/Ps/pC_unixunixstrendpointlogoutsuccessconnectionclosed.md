#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-logout-success-connectionclosed
  ParserVersion = v1.0.0
  Conditions = [ """ <sshd> """, """<Connection closed by """ ]
  Fields = ${DLUnixParsersTemplates.unix-sshd-logout.Fields}[
    """<Connection closed by ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?:?(\s|>)""",
  ]

unix-sshd-logout = {
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Fields = [
    """<({time}\d+\s+\w+\s+\d+\s+\d+:\d+:\d+)\s""",
    """({event_code}ssh)""",
    """<sshd>\s*<({event_name}[^>]+)""",
    """\d+\s+\w+\s+\d+\s+\d+:\d+:\d+\s+\w+>\s+<({dest_host}[\w\-.]+)""",
  
}
```