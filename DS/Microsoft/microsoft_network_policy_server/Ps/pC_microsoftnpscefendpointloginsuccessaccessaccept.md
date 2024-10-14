#### Parser Content
```Java
{
Name = "microsoft-nps-cef-endpoint-login-success-accessaccept"
Vendor = "Microsoft"
Product = "Microsoft Network Policy Server"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Microsoft|NPS|"""
  """|Access-Accept|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """\sdntdom=({domain}[^\s]+)"""
  """\sdestinationZoneURI=({network}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```