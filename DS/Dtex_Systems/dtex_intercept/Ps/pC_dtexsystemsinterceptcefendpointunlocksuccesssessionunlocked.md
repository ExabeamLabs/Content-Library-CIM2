#### Parser Content
```Java
{
Name = "dtexsystems-intercept-cef-endpoint-unlock-success-sessionunlocked"
  Vendor = Dtex Systems
  Product = DTEX InTERCEPT
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Dtex|""", """|SessionUnlocked|""" ]
  Fields = [
    """\Wstart=({time}\d{13})""",
    """\WDevice_Name =(({domain}[^\\]+)\\+)?({host}[^\\\s]+)""",
    """\WUser_Name =(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s""",
    """\|Dtex\|([^\|]*\|){2}(SessionActivity\|)?({event_code}[^\|]+)\|""",
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "host->dest_host" ]


}
```