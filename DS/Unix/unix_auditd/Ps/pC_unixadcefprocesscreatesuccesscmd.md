#### Parser Content
```Java
{
Name = unix-ad-cef-process-create-success-cmd
  ParserVersion = v1.0.0
  Conditions = [ """CEF""", """Unix|Unix""", """|CMD|""" ]
  Fields = ${UnixParsersTemplates.cef-unix-template.Fields}[
    """\sfname=({process_command_line}.*?)\s+\w+="""
    """\sfname=({process_path}({process_dir}\/.*?)({process_name}[^\/]*?[^\\]))((\\\\)*\s|\))"""
    """\Wcs4=({process_id}\d+)"""
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
      """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """\Wdhost=({dest_host}[\w\-.]+)""",
    
}
```