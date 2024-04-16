#### Parser Content
```Java
{
Name = tyco-ccure-kv-physical-location-access-vendoraction
  Vendor = Tyco
  Product = CCURE Building Management System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """vendor_action=""","""door_name=""","""reason_code=""" ]
  Fields = [
    """message_time=\\*"({time}\d+-\d+-\d+\s\d+:\d+:\d+)""",
    """door_name="({location_door}[^"]+)"""",
    """card_number="({badge_id}[^"]+)"""",
    """employee_id="({employee_id}[^"]+)"""",
    """last_name="({last_name}[^"]+)"""",
    """first_name="({first_name}[^"]+)"""",
    """reason_code="({action}[^"]+)"""",
    """vendor_action="({result}[^"]+)"""",
    """description="({additional_info}[^"]+)"""",
    """user="({user}[\w\.\-]{1,40}\$?)""""
  ]


}
```