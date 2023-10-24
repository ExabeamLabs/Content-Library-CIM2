#### Parser Content
```Java
{
Name = "unix-unix-json-endpoint-login-fail-failed"
Product = "Unix"
Conditions = [
  """"ident":"sshd"""
  """error: connect_to"""
  """failed"""
]
ParserVersion = "v1.0.0"

cef-unix-template.Fields}[
    """\sfname=({process_command_line}.*?)\s+\w+="""
    """\sfname=({process_path}({process_dir}\/.*?)({process_name}[^\/]*?[^\\]))((\\\\)*\s|\))"""
    """\Wcs4=({process_id}\d+)"""
  
}
```