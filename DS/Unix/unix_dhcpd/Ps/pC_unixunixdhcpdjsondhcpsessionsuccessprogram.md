#### Parser Content
```Java
{
Name = "unix-unixdhcpd-json-dhcp-session-success-program"
Vendor = "Unix"
Product = "Unix dhcpd"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"program":"dhcpd""""
  """"logT":"DHCP-LINUX""""
  """"message":"Added new forward map"""
]
Fields = [
  """exa_json_path=$.@timestamp,exa_field_name=time"""
  """exa_json_path=$.host,exa_field_name=host"""
  """exa_json_path=$.message,exa_regex=Added new forward map from ({dest_host}[^\s]+) to ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```