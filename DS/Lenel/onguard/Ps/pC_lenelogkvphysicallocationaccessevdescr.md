#### Parser Content
```Java
{
Name = "lenel-og-kv-physical-location-access-evdescr"
Vendor = "Lenel"
Product = "OnGuard"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVDESCR="""
]
Fields = [
  """EVENT_TIME_UTC=\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """EMPID=\"*({employee_id}[^,\"]*)"""
  """CARDNUM=\"*({badge_id}[^,\"]*)"""
  """UserID=\"({user}[^\"]*)"""
  """EVDESCR=\"({action}[^\"]*)"""
  """LASTNAME=\"({last_name}[^\"]*)"""
  """FIRSTNAME=\"({first_name}[^\"]*)"""
  """READERDESC=\"({location_door}[^\"]*)"""
  """, NAME=\"({location_building}[^\"]*)"""
  """, NAME=\"({location_city}[^\s-]*)"""
  """location=\"({location_city}[^. ]*)"""
  """location=\"({location_door}[^\"]*)"""
  """location=\"({location_building}[A-Z]+\s[A-Z]+)"""
  """location=\"({location_building}[\w\s-]+\.-?\d)"""
]
ParserVersion = "v1.0.0"


}
```