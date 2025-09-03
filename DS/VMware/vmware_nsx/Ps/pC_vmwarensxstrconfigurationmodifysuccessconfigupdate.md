#### Parser Content
```Java
{
Name = vmware-nsx-str-configuration-modify-success-configupdate
 ParserVersion = "v1.0.0"
 Conditions= [ """Avi-Controller""", """event CONFIG_UPDATE""" ]
 
nsx-config-change-activity = {
    Vendor = VMware
    Product = VMware NSX
    TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
    Fields = [
      """({host}[\w\-\.]+)\sAvi-Controller""",
      """event\s({operation}[^\s]+)""",
      """({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d.\d\d:\d\d)\sevent""",
      """occurred on object ({object}[^\s]+)""",
      """({result}(?i)success|failure)""",
      """tenant\s({tenant_id}[\w\-\.]+)\s""",
      """by user ({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    
}
```