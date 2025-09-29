#### Parser Content
```Java
{
Name = unix-unixauditd-str-endpoint-login-success-authenticated
  Conditions = [ """- USER""", """Authenticated without password""" ]
  Fields = ${UnixParsersTemplates.unixauditd-str-template.Fields}[
    """({event_name}Authenticated without password)"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+"""
  ]
  ParserVersion = v1.0.0


}
```