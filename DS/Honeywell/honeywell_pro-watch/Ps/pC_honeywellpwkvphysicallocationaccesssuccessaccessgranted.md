#### Parser Content
```Java
{
Name = honeywell-pw-kv-physical-location-access-success-accessgranted
  ParserVersion = v1.0.0
  Product = Honeywell Pro-Watch
  Conditions = [ """EventDescription="""", """EmployeeID="""", """Card#="""" ]

s-prowatch-badge-access-1 = {
    Vendor = Honeywell
    TimeFormat =  "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """EventDate="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
      """Card#="({badge_id}[^"]+)"""",
      """EmployeeID="({employee_id}[^"]+)"""",
      """DomainID="({domain}[^"]+)"""",
      """DoorUsed="\s*({location_door}[^"]+?)\s*"""",
      """FirstName ="\s*({first_name}[^"]+?)\s*"""",
      """LastName ="\s*({last_name}[^"]+?)\s*"""",
      """Department="\s*({location_building}[^"]+?)\s*"""",
      """EventDescription="({result}[^"]+)"""",
    
}
```