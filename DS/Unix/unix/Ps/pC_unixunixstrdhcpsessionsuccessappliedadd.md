#### Parser Content
```Java
{
Name = "unix-unix-str-dhcp-session-success-appliedadd"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """ applied ADD for """
    """IN A"""
  ]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)?\s({host}[^\s]+)\snamed\["""
    """applied ADD for '({dest_host}[^']+).+? IN A ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  ]
  DupFields = [
    "dest_host->user"
  ]
  ParserVersion = "v1.0.0"


}
```