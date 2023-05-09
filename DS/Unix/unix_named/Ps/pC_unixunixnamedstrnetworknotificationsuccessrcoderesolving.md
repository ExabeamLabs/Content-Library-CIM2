#### Parser Content
```Java
{
Name = unix-unixnamed-str-network-notification-success-rcoderesolving
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Named
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """unexpected RCODE resolving""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}\S+) named""",
    """({result}\S+)\s+({event_name}unexpected RCODE resolving)\s+\'((({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\.[^\']+?)|(({dest_host}[\w\-.]+)[^\']+?))\':\s*([^\s\#]+)\#"""
# name_server is removed
  ]


}
```