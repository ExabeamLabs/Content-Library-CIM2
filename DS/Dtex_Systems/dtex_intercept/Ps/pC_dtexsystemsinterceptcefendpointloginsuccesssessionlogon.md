#### Parser Content
```Java
{
Name = dtexsystems-intercept-cef-endpoint-login-success-sessionlogon
  Vendor = Dtex Systems
  Product = DTEX InTERCEPT
  TimeFormat = "epoch"
  Conditions = [ "CEF:", """|Dtex|""", """|SessionActivity|SessionLogon|""" ]
  Fields = [
    """\Wstart=({time}\d{13})""",
    """\WDevice_Name =(({domain}[^\\]+)\\+)?({host}[^\\\s]+)""",
    """\WUser_Name =(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s""",
    """\|Dtex\|([^\|]*\|){2}(SessionActivity\|)?({event_code}[^\|]+)\|""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```