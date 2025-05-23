#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-movetofolder
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ"]
  ExtractionType = json
  Conditions = ["""New-InboxRule""" , """MoveToFolder"""]
  Fields = [
    """timestamp="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """MoveToFolder",.+?Value":"({target}[^\s"]+)""""
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({operation}MoveToFolder)""",
    """additional_info="({additional_info}[^=]+?)(\s+\w+="|$)""",
    """msg=({additional_info}[^=]+?)\srequest=""",
    """user_email="({email_address}[^"@\s]+@({email_domain}[^"@\s]+))"""",
    """app="({app}[^"]+)"""",
    """destinationServiceName =({app}.+?)\sdevice""",
    """UserId":"(\\.+)?\/(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+))(\\)?\\"\s*on behalf""",
    """UserId":"(\\.+)?\/({last_name}[^,]+),\s*({first_name}[^\\"]+)\\"\s*on behalf"""
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^\\"]+)))"+"""
    """"SubjectOrBodyContainsWords":"({filter_key_words}[^"]+)"""
    """"Name":"MoveToFolder","Value":"({object}[^"]+?)\s*""""
    """"ObjectId":"(Unknown|Not Available|({object}[^"]+?))\s*""""
    """\ssourceServiceName =(Core Directory|Account Provisioning|({app}[^=]+?))\s+(\w+=|$)"""
    """"OriginatingServer":"({host}[\w\-.]+?)\s*\("""
    """"CorrelationId":\s*"({correlation_id}[^"]+)""""
    """exa_json_path=$..CreationTime,exa_field_name=time""",
    """exa_json_path=$..Parameters[?(@.Name == 'MoveToFolder')].Value,exa_field_name=target""",
    """exa_json_path=$..ResultStatus,exa_field_name=result""",
    """exa_json_path=$..ClientIP,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_regex=({operation}MoveToFolder)""",
    """exa_json_path=$..UserId,exa_regex=\/(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=\/]+))(\\)?\\"\s*on behalf""",
    """exa_json_path=$..UserId,exa_regex=\/({last_name}[^,\\\/]+),\s*({first_name}[^\\\/"]+)\\"\s*on behalf""",
    """exa_regex="UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^\\"]+)))"""",
    """exa_json_path=$..Parameters[?(@.Name == 'MoveToFolder')].Value,exa_field_name=object""",
    """exa_json_path=$..ObjectId,exa_field_name=object""",
    """exa_json_path=$..OriginatingServer,exa_regex=^({host}[\w\-.]+?)\s*\(""",
    """exa_json_path=$..CorrelationID,exa_field_name=correlation_id""",
    """exa_json_path=$..Parameters[?(@.Name == 'Name')].Value,exa_field_name=rule"""
  ]


}
```