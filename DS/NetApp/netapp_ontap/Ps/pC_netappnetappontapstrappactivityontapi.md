#### Parser Content
```Java
{
Name = netapp-netappontap-str-app-activity-ontapi
    Vendor = NetApp
    Product = NetApp Ontap 
    ParserVersion = v1.0.0
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """ [kern_audit:info:""" ,""":ontapi ::"""]
    Fields = [
      """\W\s*\d{1,2}\s*\d\d:\d\d:\d\d\s*({host}[\w\-\.]+):\s*""",
      """({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
      """::\s*(null|-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
      """::\s*(null|-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*::\s*[^:]+:(({domain}[^\\\s]+)\\+)?((?i)unknown|(({account}\w{3,4}\-[\w\-]+)|({user}[^\s::]+)))"""
      """::\s*({result}Success|Error):\s*({failure_reason}[^:"]+):?"""
    ]
  

}
```