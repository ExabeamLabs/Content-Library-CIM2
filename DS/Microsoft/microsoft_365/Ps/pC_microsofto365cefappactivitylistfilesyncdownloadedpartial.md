#### Parser Content
```Java
{
Name = microsoft-o365-cef-app-activity-list-filesyncdownloadedpartial
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|OneDrive|""", """|FileSyncDownloadedPartial|""" ]

cef-onedrive-app-activity-1 = {
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "epoch"
  Fields = [
    """\Wdvc=({host}\S+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wact=({operation}.+?)\s+(\w+=|$)""",
    """\Wrt=({time}\d{13})""",
    """\Wduser=({email_address}[^@\s]+@({email_domain}[^\s@]+))""",
    """\Wsuser=({email_address}[^@\s]+@({email_domain}[^\s@]+))""",
    """\Wsuid=({email_address}[^@\s]+@({email_domain}[^\s@]+))""",
    """\Woutcome=({result}.+?)\s+(\w+=|$)""",
    """CEF:([^\|]*\|){2}({app}[^\|]+)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  
}
```