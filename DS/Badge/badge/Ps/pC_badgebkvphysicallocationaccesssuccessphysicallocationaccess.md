#### Parser Content
```Java
{
Name = badge-b-kv-physical-location-access-success-physicallocationaccess
    Vendor = Badge
    Product = Badge
    TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
    Conditions = [ """, EmpID="""", """, LastAccess="""", """, Panel="""" ]
    Fields = [
      """\sEmpID="({employee_id}\d+)""",
      """\sLastAccess="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
      """\sSite="({location_city}[^"]+?)\s*"""",
      """\sPanel="({location_building}[^"]+?)\s*"""",
      """\sReader="({location_door}[^"]+?)\s*"""",
    ]
    ParserVersion = "v1.0.0"
  

}
```