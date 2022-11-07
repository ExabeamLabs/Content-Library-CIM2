#### Parser Content
```Java
{
Name = badge-b-kv-physical-location-access-success-accesssuccess
    Vendor = Badge
    Product = Badge
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """WorkerID=""", """PrimarySeatLocation="""]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """WorkerID=({employee_id}\d+)""",
      """FirstName =({first_name}.+?)\s+LastName =""",
      """LastName =({last_name}.+?)\s+WorkerID=""",
      """MessageType=({result}.+?)\s+Door=""",
      """Location="+({location_building}[^"]+)""",
      """Door="+({location_door}[^"]+)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```