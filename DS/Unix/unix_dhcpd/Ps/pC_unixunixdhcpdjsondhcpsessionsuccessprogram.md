#### Parser Content
```Java
{
Name = "unix-unixdhcpd-json-dhcp-session-success-program"
Vendor = "Unix"
Product = "Unix dhcpd"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"program":"dhcpd""""
  """"logT":"DHCP-LINUX""""
  """"message":"Added new forward map"""
]
Fields = [
  """"@timestamp":\"({time}[^\"]+)"""
  """"host":\"({host}[^\"]+)"""
  """"message":\"Added new forward map from ({dest_host}[^\s]+) to ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```