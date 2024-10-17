#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-sshdconnectionfrom"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd HH:mm:ss"]
  Conditions = [ 
    """sshd["""
    """ Connection from """
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\d\d(\dZ)?\s({host}[\w\-\.]+)(\s\w+)?\s*sshd\["""
    """({time}\w+\s\d+\s\d+:\d+:\d\d(\dZ)?)\s({host}[\w\-\.]+)(\s\w+)?\s*sshd\["""
    """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
    """\ssshd\[\d+\]:\s*({additional_info}.+?)\s*$"""
    """Connection from.*?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))((\]?:({src_port}\d+))? port\s*({=src_port}\d+))?"""
    """Connection from .*?({dest_mac}([A-Fa-f\d]+:){7}[A-Fa-f\d]+)\s*"""
  ]
  DupFields=["host->dest_host"]
  ParserVersion = "v1.0.0"


}
```