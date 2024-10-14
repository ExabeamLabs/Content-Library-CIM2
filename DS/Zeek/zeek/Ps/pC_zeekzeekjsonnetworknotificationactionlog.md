#### Parser Content
```Java
{
Name = zeek-zeek-json-network-notification-actionlog
  Vendor = Zeek
  Product = Zeek
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = ["""Notice::ACTION_LOG"""]
  Fields = [
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid":"({connection_id}[^"]+)""",
    """"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"id\.orig_p":({src_port}\d+)""",
    """"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"id\.resp_p":({dest_port}\d+)""",
    """"proto":"({protocol}[^"]+)""",
    """"msg":"({additional_info}[^"]+)""",
# peer is removed
    """"sub":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """emailAddress=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]


}
```