#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-logout-success-receiveddisconnect
  ParserVersion = v1.0.0
  Conditions = [ """ <sshd> """, """<Received disconnect from """ ]
  Fields = ${DLUnixParsersTemplates.unix-sshd-logout.Fields}[
    """<Received disconnect from ({src_ip}[A-Fa-f:\d.]+?):?(\s|>)""",
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