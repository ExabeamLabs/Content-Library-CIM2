#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-file-write-success-objectcreated
  ParserVersion = v1.0.0
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """"awsRegion"""", """"eventName":""", """"ObjectCreated:Put"""" ]
  Fields = [
      """exa_json_path=$..eventSource,exa_field_name=service_name"""
      """exa_json_path=$..awsRegion,exa_field_name=region"""
      """exa_json_path=$..eventTime,exa_field_name=time"""
      """exa_json_path=$..eventName,exa_field_name=operation"""
      """exa_json_path=$..userIdentity.principalId,exa_field_name=principal_id"""
      """exa_json_path=$..sourceIPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$..arn,exa_field_name=user_arn"""
      """exa_regex="+object.+?key\\?":\s*\\?"({file_path}(({file_dir}[^\"]+?)[\\\/]+?)?({file_name}[^"\\\/]+?(\.({file_ext}[^\.\"\\\/]+))?)?)\s*\\?""""
      """exa_json_path=$..size,exa_field_name=bytes"""
      """exa_json_path=$..bucket.name,exa_field_name=s3_bucket_name"""
  ]
 

}
```