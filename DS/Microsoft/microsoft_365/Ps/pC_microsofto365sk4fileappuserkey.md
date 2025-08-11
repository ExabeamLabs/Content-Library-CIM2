#### Parser Content
```Java
{
Name = microsoft-o365-sk4-file-app-userkey
  ParserVersion = v1.0.0
  Conditions = [ """"Workload":"""", """"UserKey":"""", """"Operation":"""" ]
  Fields = ${MSParserTemplates.o365-file-app-activity.Fields} [
      """exa_json_path=$.PolicyMatchInfo.PolicyName,exa_field_name=policy_name"""
      """exa_json_path=$.FileExtension,exa_field_name=file_ext"""
      """exa_json_path=$.Application,exa_field_name=app"""
      """exa_json_path=$.ObjectId,exa_regex=({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))$"""
      """exa_json_path=$.DeviceName,exa_field_name=src_host"""
      """exa_json_path=$.RemovableMediaDeviceAttributes.Manufacturer,exa_field_name=removable_media_vendor"""
      """exa_json_path=$.RemovableMediaDeviceAttributes.SerialNumber,exa_field_name=removable_media_serial_number"""
      """"PolicyName":\s*"({policy_name}[^"]+)""""
      """"FileExtension":\s*"({file_ext}[^"]+)""""
      """"Application":\s*"({app}[^"]+)""""
      """"ObjectId":\s*"({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))""""
      """"DeviceName":\s*"({src_host}[^"]+)""""
      """"Manufacturer":\s*"({removable_media_vendor}[^"]+)""""
      """"SerialNumber":\s*"({removable_media_serial_number}[^"]+)""""
    ]

o365-file-app-activity = {
    Vendor = Microsoft
    Product = Microsoft 365
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"Operation":\s*"({operation}[^"]+)""",
      """"UserId":\s*"({email_address}[^:@]+@({email_domain}[^",]+\.[^",]+))",""",
      """"Workload":\s*"({app}[^"]+)"""",
      """"ObjectId":\s*"({object}[^"]+)""",
      """"Id":\s*"({object_id}[^"]+)"""", 
      """"RecordType":\s*"*({object_type}[^,]+?)"*,""",
      """"ClientIP":\s*"(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\%\d+)?(:({src_port}\d+))?"""",
      """"SourceFileName":\s*"({src_file_name}[^"]+)"""",
      """"SourceRelativeUrl":\s*"({src_file_path}[^"]+)"""",
      """"SourceFileExtension":\s*"({src_file_ext}[^"]+)"""",
      """"UserAgent":\s*"({user_agent}[^"]+)""""
      """"UserType":"*({user_type}[^,}"]+)"*"""
      """exa_json_path=$.CreationTime,exa_field_name=time"""
      """exa_json_path=$.Operation,exa_field_name=operation"""
      """exa_json_path=$.UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
      """exa_json_path=$.Workload,exa_field_name=app"""
      """exa_json_path=$.ObjectId,exa_field_name=object"""
      """exa_json_path=$.Id,exa_field_name=object_id"""
      """exa_json_path=$.RecordType,exa_field_name=object_type"""
      """exa_json_path=$.ClientIP,exa_field_name=src_ip"""

}
```