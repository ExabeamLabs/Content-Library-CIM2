#### Parser Content
```Java
{
Name = "siemens-s-kv-physical-location-access-direction"
Vendor = "Siemens"
Product = "Siemens Access Control"
TimeFormat = "yyyy-MM-dd' 'HH:mm:ss.S"
Conditions = [
  """MessageType=""""
  """MessageLocaleOffset=""""
  """CardNumber=""""
  """EmployeeID=""""
  """Direction=""""
]
Fields = [
  """EmployeeID=\"({user_id}[^\"]+)\""""
  """FirstName =\"({first_name}[^\"]+)\""""
  """LastName =\"({last_name}[^\"]+)\""""
  """CardNumber=\"({badge_id}[^\"]+)\""""
  """MessageUTC=\"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d)\""""
  """MessageType=\"({action}[^\"]+)\""""
  """DoorName =\"({location_door}[^\"]+)\""""
]
ParserVersion = "v1.0.0"


}
```