#### Parser Content
```Java
{
Name = badge-b-csv-physical-location-access-success-ocardadmitted
    Vendor = Badge
    Product = Badge
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [""":0CardAdmitted;"""]
    Fields = [
      """:\d+\.\d+\.\d+\.\d+:\d[^;]+;({host}[^;\s]+);""",
      """:\d+\.\d+\.\d+\.\d+:\d({result}[^;]+);""",
      """:\d+\.\d+\.\d+\.\d+:\d[^;]+;[^;]+;({last_name}[^,]+),\s*({first_name}[^;]+)""",
      """(?:[^;]*;){3}({location_door}[^;]+)?""",
      """(?:[^;]*;){4}({user}[^;]+)?""",
      """(?:[^;]*;){3}(?:[^.]*.){3}({location_city}[^.]+)""",
      """(?:[^;]*;){3}(?:[^.]*.){4}({location_building}[^.]+)""",
      """(?:[^;]*;){3}(?:[^.]*.){5}({location_door}[^;]+)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```