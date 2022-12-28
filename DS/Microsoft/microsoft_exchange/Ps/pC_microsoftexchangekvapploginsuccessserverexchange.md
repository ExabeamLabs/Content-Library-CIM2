#### Parser Content
```Java
{
Name = microsoft-exchange-kv-app-login-success-serverexchange
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Imap4""", """Exchange Server""", """,login,""", """"R=OK""" ]
  Fields = [
    """"R=({result}OK)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)(,[^,]*){2

}
```