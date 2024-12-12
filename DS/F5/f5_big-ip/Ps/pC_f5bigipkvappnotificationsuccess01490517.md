#### Parser Content
```Java
{
Name = f5-bigip-kv-app-notification-success-01490517
  Vendor = F5
  Product = F5 BIG-IP
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """Partition="""", """session_id="""", """01490517:5:""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}(\+|-)\d{2}:\d{2})\s({host}[\w.-]+)""",
    """\][^~]+?:\s+({additional_info}[^~]+?)\s*("|$)""",
    """session_id="({session_id}[^"]+)"""
    """\sAccess_Profile="({access_group}[^"]+)""""
  ]


}
```