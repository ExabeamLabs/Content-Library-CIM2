#### Parser Content
```Java
{
Name = vmware-horizon-csv-endpoint-login-success-tunnelservice
  Vendor = VMware
  Product = VMware Horizon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Request from ""","""[TunnelService]"""]
  Fields = [
      """Request from \/({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """(?:\/(.+?\/)*[^\s]+\?[^\s]+({session_id}\w{4}))""" 
  ]
  ParserVersion = "v1.0.0"


}
```