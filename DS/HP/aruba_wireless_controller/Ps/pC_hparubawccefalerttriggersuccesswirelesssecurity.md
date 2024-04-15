#### Parser Content
```Java
{
Name = "hp-arubawc-cef-alert-trigger-success-wirelesssecurity"
Vendor = "HP"
Product = "Aruba Wireless controller"
TimeFormat = "epoch"
Conditions = [
"""|Aruba Networks"""
"""Mobility Controller"""
"""catdt=Wireless Security"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""Mobility Controller\|?.*?\|.*?\|({src_host}[^\|]+)\|"""
"""cat=({alert_name}.+?)\srt"""
"""catdt=({alert_type}[^\s]+)"""
"""\s+at=({operation}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```