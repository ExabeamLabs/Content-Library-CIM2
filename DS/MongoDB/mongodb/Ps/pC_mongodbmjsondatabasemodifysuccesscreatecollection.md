#### Parser Content
```Java
{
Name = "mongodb-m-json-database-modify-success-createcollection"
  Conditions = [ """"atype" :""", """"createCollection"""", """"ts"""", """"local" : {""", """"param" :""", """"users" : [""" ]
  ParserVersion = "v1.0.0"

mongodb-database-events = {
    Vendor = MongoDB
    Product = MongoDB
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """exa_json_path=$..['$date'],exa_field_name=time""",
      """exa_json_path=$.users[0].user,exa_field_name=user""",
      """exa_json_path=$.users[0].db,exa_field_name=db_user""",
      """exa_json_path=$.atype,exa_field_name=db_operation""",
      """exa_json_path=$.param.ns,exa_field_name=db_name""",
      """exa_json_path=$.result,exa_field_name=result""",
      """exa_json_path=$.local.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$.local.port,exa_field_name=src_port""",
      """exa_json_path=$.remote.ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """exa_json_path=$.remote.port,exa_field_name=dest_port""",
    
}
```