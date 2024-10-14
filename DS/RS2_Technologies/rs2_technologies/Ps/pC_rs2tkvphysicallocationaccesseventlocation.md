#### Parser Content
```Java
{
Name = "rs2-t-kv-physical-location-access-eventlocation"
Vendor = "RS2 Technologies"
Product = "RS2 Technologies"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Conditions = [
"""CardNumber="""
"""SiteName ="""
"""EventLocation="""
]
Fields = [
"""\sEventDate="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d)"""
"""\sSiteName ="({location_building}[^"]+)"""
"""\sEventLocation="({location_door}[^"]+)"""
"""\sEventDescription="({action}[^"]+)"""
"""\sEID="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\sCardNumber="({badge_id}[^"]+)"""
"""\sFirstName ="\s*({first_name}[^"]+?)\s*""""
"""\sLastName ="\s*({last_name}[^"]+?)\s*""""
]
ParserVersion = "v1.0.0"


}
```