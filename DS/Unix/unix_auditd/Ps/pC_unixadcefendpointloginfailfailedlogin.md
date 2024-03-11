#### Parser Content
```Java
{
Name = unix-ad-cef-endpoint-login-fail-failedlogin
  Vendor = Unix
  Product = Unix Auditd
  Conditions = [ """CEF""", """Unix|Unix""", """|failed login attempt|""" ]
  Fields = ${UnixParsersTemplates.cef-unix-template.Fields}[
     """\sduser=({user}.*?)\s+\w+="""
  ]
  ParserVersion = "v1.0.0"

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