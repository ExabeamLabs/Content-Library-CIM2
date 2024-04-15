#### Parser Content
```Java
{
Name = "unix-unix-cef-user-switch-success-userstart"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"type":"USER_START""""
  """res\=success"""
  """PAM:session_open"""
  """Cloud Apps Security|"""
  """|audit-event|"""
]
ParserVersion = "v1.0.0"

cef-unix-template.Fields}[
    """\sfname=({process_command_line}.*?)\s+\w+="""
    """\sfname=({process_path}({process_dir}\/.*?)({process_name}[^\/]*?[^\\]))((\\\\)*\s|\))"""
    """\Wcs4=({process_id}\d+)"""
  
}
```