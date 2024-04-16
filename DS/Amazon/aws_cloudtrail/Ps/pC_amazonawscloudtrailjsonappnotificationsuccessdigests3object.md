#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-app-notification-success-digests3object
  ParserVersion = v1.0.0
  Vendor = Amazon
  Product = AWS CloudTrail
  ExtractionType = json
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss" , "yyyy-MM-dd'T'HH:mm:ssZ" ]
  Conditions = [ """"previousDigestS3Object":""",""""digestPublicKeyFingerprint":"""",""""s3Bucket":"""" ]
  Fields = [
      """exa_json_path=$.digestEndTime,exa_field_name=time"""
      """exa_json_path=$.destinationServiceName,exa_field_name=app"""
      """exa_json_path=$.awsAccountId,exa_field_name=account_id"""
      """exa_json_path=$.digestSignatureAlgorithm,exa_field_name=hash_type"""
      """exa_json_path=$.digestPublicKeyFingerprint,exa_field_name=fingerprint"""
      """exa_json_path=$.previousDigestSignature,exa_field_name=sha"""
      """exa_json_path=$.digestS3Bucket,exa_field_name=bucket_name"""
 ]


}
```