#### Parser Content
```Java
{
Name = badge-b-json-physical-location-access-accessdescription
    Vendor = Badge
    Product = Badge
    TimeFormat = "MM/dd/yyyy HH:mm:ss"
    Conditions = ["""AccessDescription""","""PersonnelID"""]
    Fields = [
      """AccessFormatedTime"+:"+({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d)""",
      """AccesshostName":"({host}[^"]+)""",
      """PersonnelID":"({user}[\w\.\-]{1,40}\$?)""",
      """PersonName":"({full_name}[^"]+)""",
      """PersonID":"({employee_id}[^"]+)""",
      """AccessDescription":"({result}[^"]+)""",
      """ReaderName":"({location_city}\w+)""",
      """ReaderName":"({location_door}[^"]+)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```