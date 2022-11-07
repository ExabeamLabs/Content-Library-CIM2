#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-activity-snare
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|Security:""", """|Snare|""", """ externalId="""]
  Fields = [
    """rt=({time}\d+)""",
    """\|Security:({event_code}\d+)\|({event_name}[^\|=]+?)\|"""
    """ahost=({host}[^\s]+)"""
    """dvchost=({dest_host}[^\s]+)""",
    """(s|d)user=(-|({user}[\w\-\.\s]+(?:\w+)?\$?))\s+\w+="""
    """dntdom=({domain}.+?)\s+\w+="""
]


}
```