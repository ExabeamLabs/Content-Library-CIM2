#### Parser Content
```Java
{
Name = "unix-dhcpd-str-dhcp-session-success-forwardmap"
  Vendor = "Unix"
  Product = "Unix dhcpd"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """Added new forward map from """
  ]
  Fields = [
    """Added new forward map from ({dest_host}[\w\-.]+)\sto\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```