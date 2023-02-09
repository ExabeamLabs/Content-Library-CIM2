#### Parser Content
```Java
{
Name = unix-unix-cef-endpoint-login-success-sessionstart
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF""", """Unix|Unix""", """|Started Session|""" ]
  Fields = ${UnixParsersTemplates.cef-unix-template.Fields}[
    """of user ({user}[^\s\.]+)""",
  ]

cef-unix-template = {
    Vendor = Unix
    Product = Unix Auditd
    TimeFormat = epoch
    Fields = [
      """\Wrt=({time}\d{13})""",
      """\Wdvc=({host}[^\s]+)""",
      """\Wdvchost=({host}[^\s]+)""",
      """CEF:([^\|]*\|){4}({additional_info}[^\|]+)""",
      """CEF:([^\|]*\|){5}({event_code}[^\|]+)""",
      """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)""",
      """\WeventId=({alert_id}\d+)""",
      """\Wsuser=({user}[^\s]+)""",
      """\Wdhost=({dest_host}[\w\-.]+)""",
    
}
```