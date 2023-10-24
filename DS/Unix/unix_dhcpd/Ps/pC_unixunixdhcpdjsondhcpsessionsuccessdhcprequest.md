#### Parser Content
```Java
{
Name = "unix-unixdhcpd-json-dhcp-session-success-dhcprequest"
Vendor = "Unix"
Product = "Unix dhcpd"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"program":"dhcpd""""
  """"logT":"DHCP-LINUX""""
  """"message":"DHCPREQUEST"""
]
Fields = [
  """"@timestamp":"({time}[^"]+)"""
  """"host":"({host}[^"]+)"""
  """"message":"DHCPREQUEST for ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?( \(({dest_host}[^\s\)]+)\))? from ({dest_mac}\S+)( \(({=dest_host}[^\s\)]+)\))? via ({dest_interface}[^\\"]+)"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```