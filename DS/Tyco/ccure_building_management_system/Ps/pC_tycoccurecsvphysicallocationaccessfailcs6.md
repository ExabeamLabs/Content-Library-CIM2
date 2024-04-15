#### Parser Content
```Java
{
Name = "tyco-ccure-csv-physical-location-access-fail-cs6"
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""requestClientApplication=CCure"""
"""cs6="""
]
Fields = [
"""cs6=({time}\d+-\d+-\d+\s\d+:\d+:\d+),(|({door_name}[^,]+)),(|({location_door}[^,]+)),(|({result}[^,]+)),(|({user}[^,]+)),(|({badge_id}\d+)),(|({first_name}[^,]+)),(|({last_name}[^,]+)),[^,]*,[^,]+,(|({full_name}[^,]+)),(|None|({employee_type}[^,]+)),(\"+)?(|({employee_title}[^,]+)),"""
"""cs6=\d+-\d+-\d+\s\d+:\d+:\d+,([^,]+,){12}(.+?\"+,)?(|({email_address}[^,]+)),(|({department}[^,]+)),(|({employee_status}[^,]+)),"""
]
ParserVersion = "v1.0.0"


}
```