#### Parser Content
```Java
{
Name = "microsoft-exchange-cef-app-activity-exchangeonline"
Conditions = [
  """CEF:"""
  """|Exchange Online|"""
  """|Create|"""
]
ParserVersion = "v1.0.0"

cef-azure-onedrive-account-password = {
  Vendor = Microsoft
  Product = Microsoft CAS
  TimeFormat = "epoch"
  Fields = [
    """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|""",
    """\|SIEM_Agent\|[^\|]*\|({event_name}[^\|]+)\|""",
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """destinationServiceName =({app}.+?)\s+(\w+=|$)""",
    """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """\Wsuser=({email_address}[^@\s]+@[^@\s]+)\s+(\w+=|$)""",
    """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\Wmsg=({additional_info}.*?)\s+(\w+=|$)""",
  
}
```