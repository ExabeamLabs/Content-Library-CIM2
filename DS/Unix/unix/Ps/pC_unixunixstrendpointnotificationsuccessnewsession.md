#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-notification-success-newsession"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ 
    """ systemd-"""
    """ New session """
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """({time}\d\d\d\d-\d+-\d+T\d\d:\d\d:\d\d\.\d+[-+]\d\d:\d\d)\s+({host}[\w.\-]+)""",
    """({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)\s*(\d+|({host}[\w\-.]+))(\s\w+)?\s*(systemd-)"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+"""
    """New\s+session\s+({session_id}[^\s]+)\s+of\s+user\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\."""
  ]
  ParserVersion = "v1.0.0"


}
```