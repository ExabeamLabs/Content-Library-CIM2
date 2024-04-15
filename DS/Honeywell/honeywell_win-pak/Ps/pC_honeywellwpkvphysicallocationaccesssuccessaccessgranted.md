#### Parser Content
```Java
{
Name = "honeywell-wp-kv-physical-location-access-success-accessgranted"
Vendor = "Honeywell"
Product = "Honeywell WIN-PAK"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Winpak - Access Granted"""
""" Name:"""
""" FirstName:"""
""" LastName:"""
]
Fields = [
"""\sGenTime:\s*"({time}\d\d\d\d-\d\d-\d\d\s+\d+:\d\d:\d\d)\.\d+""""
"""\sParam3:\s*"({badge_id}\d+)""""
"""\sName:\s*"({location_door}.+?)""""
"""\sFirstName:\s*"({first_name}.+?)""""
"""\sLastName:\s*"({last_name}.+?)""""
"""({action}Access Granted)"""
]
ParserVersion = "v1.0.0"


}
```