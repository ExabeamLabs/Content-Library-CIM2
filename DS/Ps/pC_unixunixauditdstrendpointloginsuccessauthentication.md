#### Parser Content
```Java
{
Name = unix-unixauditd-str-endpoint-login-success-authentication
  Conditions = [ """- USER""", """TLSUserName authentication successful""" ]
  Fields = ${UnixParsersTemplates.unixauditd-str-template.Fields}[
    """({event_name}TLS/X509 TLSUserName authentication successful)"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+"""
  ]
  ParserVersion = v1.0.0


}
```