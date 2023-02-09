#### Parser Content
```Java
{
Name = pan-cortex-cef-endpoint-notification-success-cortexxdragent
  Vendor = Palo Alto Networks
  Product = Cortex XDR
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """|Palo Alto Networks|""", """|Cortex XDR Agent|""", """|Agent Audit Logs|""" ]
  Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
  """dvchost=({host}[^\s]+)""",
  """shost=({src_host}[^\s]+)""",
  """cat=({category}[^\s]+)""",
  """msg=({additional_info}.+?)\s+(\w+=|$)""",
  ]


}
```