#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-activity-microsoftwindowssecurityauditing
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|Microsoft-Windows-Security-Auditing""", """|Snare|""", """ externalId="""]
  Fields = [
    """\srt=({time}\d{13})""",
    """\|Microsoft-Windows-Security-Auditing:({event_code}\d+)\|({event_name}[^\|=]+?)\|"""
    """ahost=({host}[^\s]+)"""
    """dvchost=({dest_host}[\w\-.]+)""",
    """(s|d)user=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"=]+))\s+\w+="""
    """dntdom=({domain}.+?)\s+\w+="""
  ]


}
```