#### Parser Content
```Java
{
Name = unix-unix-sk4-endpoint-authentication-useracct
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"type":"USER_ACCT"""", """res\=success""", """PAM:accounting""", """Cloud Apps Security|""", """|audit-event|""" ]

unix-template-dl = {
    Vendor = Unix
    Product = Unix Auditd
    TimeFormat = epoch
    Fields = [
      """\Wrt=({time}\d{13})""",
      """\Wdvc=({host}[^\s]+)""",
      """\Wdvchost=({host}[^\s]+)""",
      """CEF:([^\|]*\|){4}({additional_info}[^\|]+)""",
      """CEF:([^\|]*\|){5}({event_code}[^\|]+)""",
      """\WeventId=({alert_id}\d+)""",
      """\Wsuser=({user}[^\s]+)""",
    
}
```