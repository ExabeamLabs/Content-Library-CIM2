#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-activity-sudo"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ 
    """sudo:"""
    """ PAM """ 
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\d\d:\d\d:\d\d ({host}\S+)? sudo:"""
    """\ssudo:\s*({additional_info}.+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```