#### Parser Content
```Java
{
Name = microsoft-exchange-str-app-activity-success-isaweblog
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ISAWebLog""" ]
  Fields = [
    """ISAWebLog\s[^\s]+\s({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """ISAWebLog\s([^\s]+\s){2}\(\w+\)({user}.+?)\s""",
    """ISAWebLog\s([^\s]+\s){6}(?:-|({app}.+?))\s""",
    """ISAWebLog\s([^\s]+\s){12}(?:-|({operation}.+?))\s""",
    """Cmd=({operation}.+?)(\s|&)""",
    """ISAWebLog\s([^\s]+\s){7}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """ISAWebLog\s([^\s]+\s){13}(?:-|({additional_info}.+?))\s""",
    """DeviceType=({src_host}[^&\s]+)"""
    """User=({domain}[^%]+)%5C"""
  ]


}
```