#### Parser Content
```Java
{
Name = unix-unix-sk4-endpoint-notification-proctitle
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"type":"PROCTITLE"""", """"proctitle""", """Cloud Apps Security|""", """|audit-event|""" ]
  Fields = ${DLUnixParsersTemplates.unix-template-dl.Fields}[
# proctitle is removed
    """message":"({event_name}[^"]+)""""
  ]

unix-template-dl = {
    Vendor = Unix
    Product = Unix Auditd
    TimeFormat = epoch
    Fields = [
      """\Wrt=({time}\d+)""",
      """\Wdvc=({host}[^\s]+)""",
      """\Wdvchost=({host}[^\s]+)""",
      """CEF:([^\|]*\|){4}({additional_info}[^\|]+)""",
      """CEF:([^\|]*\|){5}({event_code}[^\|]+)""",
      """\WeventId=({alert_id}\d+)""",
      """\Wsuser=({user}[^\s]+)""",
    
}
```