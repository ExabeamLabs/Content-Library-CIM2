#### Parser Content
```Java
{
Name = microsoft-exchange-kv-app-login-fail-imap4
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Imap4""", """Exchange Server""", """,login,""", """"R="""" ]
  Fields = [
    """({event_name}LOGIN ({result}failed))""",
    """Error="+({failure_reason}[^"-]+?)\s*[\-"]""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)(,[^,]*){2

}
```