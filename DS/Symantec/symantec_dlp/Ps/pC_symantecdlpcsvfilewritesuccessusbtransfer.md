#### Parser Content
```Java
{
Name = symantec-dlp-csv-file-write-success-usbtransfer
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """USB Transfer""", """Endpoint """ ]
  Fields = [
    """>\w+ \d\d \d\d:\d\d:\d\d\s+({host}\S+?)\s+\S+\s*(?:;|,)[^;,]*(?:;|,)\s*({dest_host}[^;,]+?)\s*(?:;|,)\s*({process_name}[^;,]+?)\s*(?:;|,)[^;,]*?(?:;|,)\s*({file_name}[^;,]+?)\s*(;|,)\s*({device_type}Endpoint[^;,]+?)\s*(?:;|,)([^;,]*(?:;|,)){2}\s*(?:({domain}[^;,\\\/]+?)[\\\/]+)?({user}[^;,\\\/]*?)\s*(?:;|,)""",
    """>\w+ \d\d \d\d:\d\d:\d\d\s+({host}\S+?)\s+\S+\s*(?:;|,)\s*({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*(?:;|,)\s*({process_name}[^;,]+?)\s*(?:;|,)[^;,]*?(?:;|,)\s*({file_name}[^;,]+?)\s*(;|,)\s*({device_type}Endpoint[^;,]+?)\s*(?:;|,)\s*({severity}[^;,]+?)\s*(?:;|,)\s*[^;,]*(?:;|,)\s*(?:({domain}[^;,\\\/]+?)[\\\/]+)?({user}[^;,\\\/]*?)\s*(?:;|,)"""
  ]
  ParserVersion = "v1.0.0"


}
```