#### Parser Content
```Java
{
Name = unix-unixauditd-str-endpoint-login-success-authentication
  Conditions = [ """- USER""", """TLSUserName authentication successful""" ]
  Fields = ${UnixParsersTemplates.unixauditd-str-template.Fields}[
    """({event_name}TLS/X509 TLSUserName authentication successful)"""
  ]
  ParserVersion = v1.0.0


}
```