#### Parser Content
```Java
{
Name = "mongodb-m-json-database-modify-success-createcollection"
  Conditions = [ """"atype" :""", """"createCollection"""", """"ts"""", """"local" : {""", """"param" :""", """"users" : [""" ]
  ParserVersion = "v1.0.0"

mongodb-database-events = {
    Vendor = MongoDB
    Product = MongoDB
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"\$date"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}[+\-]\d{1,4})""",
      """"user"\s*:\s*"({user}[\w\.\-]{1,40}\$?)"""",
      """"users"\s*:\s*\[[^\]]+"db"\s*:\s*"({db_user}[^"]+)"""",
      """"atype"\s*:\s*"({db_operation}[^"]+)"""",
      """"ns"\s*:\s*"({db_name}[^"\.]+)""",
      """"result"\s*:\s*({result}[^\}]+?)\s*\}""",
      """"local"\s*:\s*\{\s*"ip"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"local"\s*:\s*\{[^\}]+?"port"\s*:\s*({src_port}\d+)""",
      """"remote"\s*:\s*\{\s*"ip"\s*:\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """"remote"\s*:\s*\{[^\}]+?"port"\s*:\s*({dest_port}\d+)"""
    
}
```