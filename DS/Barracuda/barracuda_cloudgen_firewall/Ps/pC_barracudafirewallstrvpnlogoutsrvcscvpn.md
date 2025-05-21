#### Parser Content
```Java
{
Name = "barracuda-firewall-str-vpn-logout-srvcscvpn"
Vendor = "Barracuda"
Product = "Barracuda Cloudgen Firewall"
ParserVersion = "v1.0.0"
TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd HH:mm:ss"]
Conditions = [
  """/srv_CSC_VPN: """
]
Fields = [
  """({time}\w+\s\d+\s\d\d:\d\d:\d\d)\s({host}[\w\_\.]+)\s\w+\/({event_name}srv_CSC_VPN):\s[\d\-:]+\s\w+\s\w+\s({protocol}\w+)\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?:\s*({additional_info}.+?\(({failure_reason}[^"]*)\)[\s"\$]+)"""
]


}
```