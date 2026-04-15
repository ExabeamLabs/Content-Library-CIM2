#### Parser Content
```Java
{
Name = netapp-netappontap-str-endpoint-login-fail-loginattempterror
    Vendor = NetApp
    Product = NetApp Ontap 
    ParserVersion = v1.0.0
    TimeFormat = "MMM dd yyyy HH:mm:ss ZZZZ"
    Conditions = [ """ [kern_audit:info:""" ,"""Login Attempt :: Error"""]
    Fields = [
      """({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\s+(\+|\-)\d\d:\d\d)""",
      """::\s*({host}[^:]+):(({domain}[^\\\s]+)\\+)?(unknown|(({account}\w{3,4}\-[\w\-]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+::\s+({action}[^:]+)\s+::"""
      """::\s*({result}Error):"""
      """:: Error:\s*({failure_reason}[^".\n]+)"""
    ]
  

}
```