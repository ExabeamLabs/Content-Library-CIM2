#### Parser Content
```Java
{
Name = "badgepoint-b-kv-physical-location-access-readerid"
Vendor = "Badgepoint"
Product = "Badgepoint"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
"""BadgeNumber=""""
"""BadgeStatus=""""
"""ReaderID=""""
]
Fields = [
"""({host}[\w\-.]+)\s+\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+"""
"""Date="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)"""
"""\WReaderDescription="({location_full}[^"]*?\s*({location_door}[^"\-]+?))""""
"""\WFacilityDescription="({location_building}[^"]+)"""
"""\WBadgeStatus="({action}[^"]+)"""
"""\WFacilityID="({facility_id}[^"]+)"""
"""\WReaderID="({location_door_id}[^"]+)"""
"""\WTransactionType="({result_code}[^"]+)"""
"""\WEmployeeNumber="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\WBadgeNumber="({badge_id}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```