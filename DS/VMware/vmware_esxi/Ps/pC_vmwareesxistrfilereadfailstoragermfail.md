#### Parser Content
```Java
{
Name = vmware-esxi-str-file-read-fail-storagermfail
  ParserVersion = v1.0.0
  Conditions = [ """storageRM[""" , """]: open """, """ failed: """ ]
  Fields = ${VMWareParsersTemplates.vmware-system-events.Fields}[
    """failed:\s*({failure_reason}[^$]+?)\s*$"""
  ]

vmware-system-events = {
    Vendor = VMware
    Product = VMware ESXi
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
      """\d\d:\d\d:\d\d\.\d{1,3}Z\s({host}[^\s]+)""",
      """storageRM\[[^\]]+\]:\s*({additional_info}[^$]+?)\s*$""",
    
}
```