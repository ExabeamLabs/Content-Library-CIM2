#### Parser Content
```Java
{
Name = symantec-wss-sk4-http-session-observed
  Vendor = Symantec
  Product = Symantec WSS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd, HH:mm:ss"
  Conditions = [ """destinationServiceName =Symantec WSS""", """, OBSERVED,"""]
  Fields = [
    """cs6=\[[^,]+,\s({time}\d\d\d\d-\d\d-\d\d,\s\d\d:\d\d:\d\d)""",
    """cs6=\[([^,]+,){3}\s({host}[^,]+)""",
    """\sdproc=(|({process_name}[^=]+?))\s+\w+=""",
    """,\s(Unauthenticated User|-|({user}[^,]+))(,\s[^,]+){2

}
```