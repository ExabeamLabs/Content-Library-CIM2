#### Parser Content
```Java
{
Name = zscaler-ia-kv-endpoint-notification-success-zia
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """|Zscaler-ZIA-Admin-Logs|""",""" category=""","""interface=""","""auditlogtype=""","""adminid=""", ]
  Fields = [
    """time=\w{1,3}\s({time}\w{1,3}\s{1,5}\d{1,2}\s\d\d:\d\d:\d\d\s\d{4})"""
    """\saction=({action}[^=]+?)\s*(\w+=|$)"""
    """clientip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """category=({category}.*?)\s+(\w+=|$)"""
    """result=({result}[^=]+?)\s*(\w+=|$)"""
    """resource=\s*({resource}[^=]+?)(\s+\w+=|\s*$)"""
]


}
```