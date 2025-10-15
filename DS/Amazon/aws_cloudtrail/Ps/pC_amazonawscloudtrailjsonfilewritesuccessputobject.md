#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-file-write-success-putobject
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ssZ"""
  ParserVersion = "v1.0.0"
  ExtractionType = json
  Conditions = [ """"source":"aws.s3"""", """"PutObject"""", """"resources":""" ] 
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.detail.reason,exa_field_name=operation""",
    """exa_json_path=$.detail.source-ip-address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.detail.object.key,exa_field_name=object""",
    """exa_json_path=$.detail.bucket.name,exa_field_name=bucket_name""",
    """exa_json_path=$.region,exa_field_name=region""",
    """exa_json_path=$.account,exa_field_name=aws_account""",
    """exa_json_path=$.detail-type,exa_field_name=event_name""",
    """exa_json_path=$.account,exa_field_name=aws_account""",
    """exa_json_path=$.resources,exa_regex=[^\]]+?Object[^\}]+?(?:ARN|arn)\\?":\s*\\?"({file_arn}[^"]+)""",
    """exa_json_path=$.resources,exa_regex=[^\]]+?Bucket[^\}]+?(?:ARN|arn)\\?":\s*\\?"({bucket_arn}[^"]+)""",
    """exa_json_path=$.resources,exa_field_name=additional_info"""          
  ]
} 

${AwsParserTemplates.aws-cloudtrail-json}{
  Name = amazon-awscloudtrail-json-image-create-awsapicall
  Vendor = Amazon
  Product = AWS CloudTrail
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """AwsApiCall""", """"eventName":""", """"CreateImage"""" ] 
  Fields = ${AwsParserTemplates.aws-cloudtrail-json.Fields}[
      """exa_json_path=$.requestParameters,exa_regex=({src_resource_type}[Ss]napshot|[Ii]nstance)Id\\?":\s*\\?"({src_resource}[^",]+?)\\?""""
      """exa_json_path=$..requestParameters.name,exa_field_name=image_name"""
      """exa_json_path=$..description,exa_field_name=description"""
      """exa_json_path=$..imageId,exa_field_name=resource_id"""
  ]


}
```