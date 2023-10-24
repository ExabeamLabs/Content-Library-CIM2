#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-sshdconnectionfrom"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
    """sshd["""
    """ Connection from """
  ]
  Fields = [
    """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
    """({host}\S+) sshd\["""
    """\ssshd\[\d+\]:\s*({additional_info}.+?)\s*$"""
    """Connection from.*?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))((\]?:({dest_port}\d+))? port\s*({=dest_port}\d+))?"""
    """Connection from .*?({dest_mac}([A-Fa-f\d]+:){7}[A-Fa-f\d]+)\s*"""
  ]
  DupFields=["host->src_host"]
  ParserVersion = "v1.0.0"


}
```