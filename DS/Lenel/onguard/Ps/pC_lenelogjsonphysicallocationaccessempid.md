#### Parser Content
```Java
{
Name = "lenel-og-json-physical-location-access-empid"
Vendor = "Lenel"
Product = "OnGuard"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """ Event_Time_CST:"""
  """ Emp_Id:"""
  """ Lnl_Emp_Id:"""
]
Fields = [
  """Event_Time_CST:\s*\"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)\"*"""
  """First_Name:\s*\"*(|({first_name}.+?))\"+(\s+\w+:|\s*\"*$)"""
  """Last_Name:\s*\"*(|({last_name}.+?))\"+(\s+\w+:|\s*\"*$)"""
  """Event_Desc:\s*\"*(|({action}.+?))\"+(\s+\w+:|\s*\"*$)"""
  """Lnl_Emp_Id:\s*\"+(|({badge_id}.+?))\"+(\s+\w+:|\s*\"*$)"""
  """\sEmp_Id:\s*\"+(|({user}.+?))\"+(\s+\w+:|\s*\"*$)"""
  """Reader_Desc:\s*\"+(|({location_door}[^\"]+))\"+(\s+\w+:|\s*\"*$)"""
]
ParserVersion = "v1.0.0"


}
```