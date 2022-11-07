#### Parser Content
```Java
{
Name = microsoft-onedrive-cef-app-activity-list-filesyncdownloadedpartial
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|OneDrive|""", """|FileSyncDownloadedPartial|""" ]

cef-onedrive-app-activity-1 = {
  Vendor = Microsoft
  Product = OneDrive
  TimeFormat = "epoch"
  Fields = [
    """\Wdvc=({host}\S+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wact=({operation}.+?)\s+(\w+=|$)""",
    """\Wrt=({time}\d+)""",
    """\Wduser=({email_address}[^@\s]+@({email_domain}[^\s@]+))""",
    """\Wsuser=({email_address}[^@\s]+@({email_domain}[^\s@]+))""",
    """\Wsuid=({email_address}[^@\s]+@({email_domain}[^\s@]+))""",
    """\Woutcome=({result}.+?)\s+(\w+=|$)""",
    """CEF:([^\|]*\|){2}({app}[^\|]+)""",
  
}
```