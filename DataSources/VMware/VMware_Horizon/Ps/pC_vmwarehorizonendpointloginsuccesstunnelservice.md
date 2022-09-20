#### Parser Content
```Java
{
Name = vmware-horizon-endpoint-login-success-tunnelservice
  Vendor = VMware
  Product = VMware Horizon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Request from ""","""[TunnelService]"""]
  Fields = [
      """Request from \/({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """(?:\/(.+?\/)*[^\s]+\?[^\s]+({session_id}\w{4}))""" 
  ]
  ParserVersion = "v1.0.0"


}
```