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
    """ISAWebLog\s[^\s]+\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """ISAWebLog\s([^\s]+\s){2}\(\w+\)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s""",
    """ISAWebLog\s([^\s]+\s){6}(?:-|({app}.+?))\s""",
    """ISAWebLog\s([^\s]+\s){12}(?:-|({operation}.+?))\s""",
    """Cmd=({operation}.+?)(\s|&)""",
    """ISAWebLog\s([^\s]+\s){7}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """ISAWebLog\s([^\s]+\s){13}(?:-|({additional_info}.+?))\s""",
    """DeviceType=({src_host}[^&\s]+)"""
    """User=({domain}[^%]+)%5C"""
  ]


}
```