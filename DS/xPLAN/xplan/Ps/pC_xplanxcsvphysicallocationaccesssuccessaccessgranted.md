#### Parser Content
```Java
{
Name = xplan-x-csv-physical-location-access-success-accessgranted
    Vendor = xPLAN
    Product = xPLAN
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """,Access granted,"""]
    Fields = [
      """,(|((?:Ms|Miss|Mrs|Mr|Dr)\s*)?(|(({full_name}({first_name}[^",\s]+)\s*({last_name}[^,"\s]*)))|[^,]+))\s*,[^,]*,(|({location_door}[^,]+?))\s*,(|({event_code}[^,]+)),({event_name}Access granted)(,[^,]*){4

}
```