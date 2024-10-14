#### Parser Content
```Java
{
Name = dg-ep-cef-endpoint-login-success-userlogon
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "epoch"
  Conditions = [ """|Digital Guardian|Digital Guardian|""", """|User Logon|""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """\sshost=(([^\/\\=]+)[\/\\]+)?({host}\S+)""",
    """\ssuser=(({domain}[^\/\\=]+)[\/\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(ad\.\S+=|\w+=|$)""",
    """\ssproc=({process_name}.+?)\s+(ad\.\S+=|\w+=|$)""",
    """({event_code}User Logon)""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```