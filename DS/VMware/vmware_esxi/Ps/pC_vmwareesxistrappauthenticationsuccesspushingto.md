#### Parser Content
```Java
{
Name = vmware-esxi-str-app-authentication-success-pushingto
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """vmware""", """vsphere""", """ Pushing """, """ to """ ]
  Fields = [
    """\d\d:\d\d\s({host}[\w\-\.]+).*?\[({time}\d{4}\-\d{1,2}\-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,3}Z).* Pushing\s({additional_info}[^"]+?)\s*("|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```