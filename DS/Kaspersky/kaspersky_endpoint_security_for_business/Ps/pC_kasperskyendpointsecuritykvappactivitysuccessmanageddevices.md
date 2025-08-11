#### Parser Content
```Java
{
Name = "kaspersky-endpointsecurity-kv-app-activity-success-manageddevices"
  Vendor = "Kaspersky"
  Product = "Kaspersky Endpoint Security for Business"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ KES|""", """gn="Managed devices"""", """ tdn="""", """etdn="""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ) ({host}[\w\-.]+) KES\|"""
    """gn="({category}[^"]+)"""
    """tdn="({operation}[^"]+)"""
    """etdn="({operation_details}[^"]+)"""
    """hdn="({src_host}[^"]+)"""
    """hip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """et="({additional_info}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```