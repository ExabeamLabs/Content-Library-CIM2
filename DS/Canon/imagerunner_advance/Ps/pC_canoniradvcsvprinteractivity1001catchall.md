#### Parser Content
```Java
{
Name = canon-iradv-csv-printer-activity-1001-catchall
   ParserVersion = v1.0.0
   Conditions = [ """-  1001,""", """iR-ADV""" ]
 
canon-endpoint-events = {
    Vendor = "Canon"
    Product = "imageRUNNER ADVANCE"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Fields = [
      """\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})) - - \d+ -\s*({event_code}\d+)"""
      """-  ({event_code}4098|1001),({product_name}[^,]+),({serial_num}[^,]+),({device_name}({printer_name}[^,]+)),(\d+)?,(|[-]+|({full_name}\w+ \w+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),(|({domain}[^,]+)),({result}[^,]+),,({operation}[^,]+),(|({resource_type}[^,]+)),,(|\d+),((|[^,]+),){2}({file_name}[^,]+)?"""
      """-  ({event_code}8193),({product_name}[^,]+),({serial_num}[^,]+),({device_name}[^,]+),,([-]+),,[-]+,[^,]+,({operation}[^,]+),(|(\w+)),(|[,]+),(\d+),([^,]+,){2}((|[^,]+),){6}(|[-]+|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)):({full_name}\w+ \w+)"""
    ]
      ParserVersion = "v1.0.0"
  
}
```