#### Parser Content
```Java
{
Name = "unix-unix-cef-process-create-success-syscall"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"type":"SYSCALL""""
  """success\=yes"""
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