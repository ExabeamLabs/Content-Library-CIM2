#### Parser Content
```Java
{
Name = cisco-asa-str-http-session-success-716003
  ParserVersion  = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-716003""", """WebVPN access GRANTED""" ]
  Fields = [
	"""({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d) ({host}[\w\-.]+) : %ASA-\d+-({event_code}\d+): .+? User <({email_address}[^>]+)> IP <({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?> ({event_name}WebVPN access ({action}[^:]+)):\s*(-|({url}({protocol}[^:\\\/]+):[\\\/]+({web_domain}[^\\\/:]+)({uri_path}\/[^\s\?]*)?({uri_query}\?[^\s]+)?))""",
   ]


}
```