#### Parser Content
```Java
{
Name = netapp-netappontap-str-endpoint-success-logging
    Vendor = NetApp
    Product = NetApp Ontap
    ParserVersion = v1.0.0
    TimeFormat = "MMM dd yyyy HH:mm:ss ZZZZ"
    Conditions = [ """ [kern_audit:info:""", """Logging""" ,"""Success""" ]
    Fields = [
      """({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\s+(\+|\-)\d\d:\d\d)""",
      """::\s*(null|-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*::\s*({host}[^:]+):(({domain}[^\\\s]+)\\+)?(unknown|(({account}\w{3,4}\-[\w\-]+)|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))"""
      """\s+({event_name}[^:]+)\s+::\s*({result}Success)"""
    ]
  

}
```