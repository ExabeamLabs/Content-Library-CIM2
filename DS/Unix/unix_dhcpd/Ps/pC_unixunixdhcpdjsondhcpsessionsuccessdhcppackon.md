#### Parser Content
```Java
{
Name = "unix-unixdhcpd-json-dhcp-session-success-dhcppackon"
Vendor = "Unix"
Product = "Unix dhcpd"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"program":"dhcpd""""
  """"logT":"DHCP-LINUX""""
  """"message":"DHCPACK on"""
]
Fields = [
  """exa_json_path=$.@timestamp,exa_field_name=time"""
  """exa_json_path=$.host,exa_field_name=host"""
  """exa_regex="message":"DHCPACK on ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? to ({dest_mac}\S+)( \(({dest_host}[^\s\)]+)\))? via ({dest_interface}[^\\"]+)"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```