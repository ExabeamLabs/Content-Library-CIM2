#### Parser Content
```Java
{
Name = hp-safecom-json-printer-activity-success-5291
Vendor = "HP"
Product = "HP SafeCom"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"run_id""""
  """"print_size""""
  """"userid""""
  """"employee_cms_code""""
  """"day_of_week""""
]
Fields = [
  """"date_part":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""
  """"userid":"({user}[^"]+)"""
  """"printer_name":"({printer_name}.+?)\s*""""
  """"pages_printed":({num_pages}\d+)"""
  """"document_details":"({object}.+?)\s*""""
  """"employee_cms_code":"({user_id}\d+)"""
  """"print_size":({bytes}\d+)"""
]
DupFields = [
  "printer_name->dest_host"
]
ParserVersion = "v1.0.0"


}
```