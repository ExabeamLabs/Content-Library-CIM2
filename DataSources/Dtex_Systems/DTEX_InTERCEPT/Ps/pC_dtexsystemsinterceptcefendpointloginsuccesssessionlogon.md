#### Parser Content
```Java
{
Name = dtexsystems-intercept-cef-endpoint-login-success-sessionlogon
  Vendor = Dtex Systems
  Product = DTEX InTERCEPT
  TimeFormat = "epoch"
  Conditions = [ "CEF:", """|Dtex|""", """|SessionActivity|SessionLogon|""" ]
  Fields = [
    """\Wstart=({time}\d+)""",
    """\WDevice_Name =(({domain}[^\\]+)\\+)?({host}[^\\\s]+)""",
    """\WUser_Name =(({domain}[^\\]+)\\+)?({user}[^\\\s]+)\s""",
    """\|Dtex\|([^\|]*\|){2}(SessionActivity\|)?({event_code}[^\|]+)\|""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```