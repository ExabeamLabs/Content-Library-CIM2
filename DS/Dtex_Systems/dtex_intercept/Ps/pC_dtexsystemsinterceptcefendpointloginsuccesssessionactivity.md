#### Parser Content
```Java
{
Name = "dtexsystems-intercept-cef-endpoint-login-success-sessionactivity"
Vendor = "Dtex Systems"
Product = "DTEX InTERCEPT"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Dtex|"""
  """|SessionActivity|SessionRemoteConnected|"""
]
Fields = [
  """\Wstart=({time}\d{13})"""
  """\WDevice_Name =(({domain}[^\\]+)\\+)?({host}[^\\\s]+)"""
  """\WUser_Name =(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
  """\|Dtex\|([^\|]*\|){2}(SessionActivity\|)?({event_code}[^\|]+)\|"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```