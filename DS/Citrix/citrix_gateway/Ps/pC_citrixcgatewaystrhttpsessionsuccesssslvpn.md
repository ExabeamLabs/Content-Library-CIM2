#### Parser Content
```Java
{
Name = "citrix-cgateway-str-http-session-success-sslvpn"
Vendor = "Citrix"
Product = "Citrix Gateway"
TimeFormat = "MM/dd/yyyy:HH:mm:ss"
Conditions = [
  """ SSLVPN """
  """ HTTPREQUEST """
]
Fields = [
  """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s*(\w\w\w)?\s+({host}[\w.\-]+)(\s+\S+){3}\s+({event_category}SSLVPN HTTPREQUEST)?.*?Context\s*(({email_address}[^@]+@[^@]+)|(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({=user}[^@]+))@({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+-\s*SessionId:\s+({session_id}[^\s]+)\s*-\s*(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({web_domain}[^\s]+))\s+User.*?\s*Vserver\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+).*?SSO[^:]+:\s*({method}[^\s]+)\s+({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?\s+"""
  """({event_name}HTTPREQUEST)"""
]
ParserVersion = "v1.0.0"


}
```