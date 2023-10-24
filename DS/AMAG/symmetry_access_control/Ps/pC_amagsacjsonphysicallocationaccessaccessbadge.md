#### Parser Content
```Java
{
Name = "amag-sac-json-physical-location-access-accessbadge"
Vendor = "AMAG"
Product = "Symmetry Access Control"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"access_badge""""
  """"txnconditionname":""""
  """"cardnumber":"""
]
Fields = [
  """"datetimeoftxn\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """"txnconditionname\":\"({action}[^\"]+)"""
  """"wherename\":\"({location_door}[^\"]+)"""
  """"firstname\":\"({first_name}[^\"]+)"""
  """"lastname\":\"({last_name}[^\"]+)"""
  """"cardnumber\":({badge_id}\d+)"""
  """"db_name\":\"({direction}[^\"]+)"""
  """"db_ip\":\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```