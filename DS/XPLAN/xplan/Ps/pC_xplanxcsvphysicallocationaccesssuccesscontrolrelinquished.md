#### Parser Content
```Java
{
Name = xplan-x-csv-physical-location-access-success-controlrelinquished
    Vendor = XPLAN
    Product = XPLAN
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """,Remote door control relinquished,"""]
    Fields = [
      """(|((?:Ms|Miss|Mrs|Mr|Dr)\s*)?(|(({full_name}({first_name}[^",\s]+)\s*({last_name}[^,"\s]*)))|[^,]+))\s*,[^,]*,(|({location_door}[^,]+?))\s*,(|({event_code}[^,]+)),({event_name}Remote door control relinquished)(,[^,]*){4

}
```