#### Parser Content
```Java
{
Name = "unix-unixdhcpd-str-dhcp-session-success-dhcpd"
Vendor = "Unix"
Product = "Unix dhcpd"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ dhcpd: """
  """ Forward map from """
]
Fields = [
  """\d\d:\d\d:\d\d\s+({host}.+?)\s+dhcpd: Forward map from ({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?)) to ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+({additional_info}.+?)\.\s*(\w+=|'|"|$)"""
]
ParserVersion = "v1.0.0"


}
```