#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-file-write-success-objectcreated
  ParserVersion = v1.0.0
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"awsRegion"""", """"eventName":"ObjectCreated:Put"""" ]
  Fields = [
  """"eventSource"+\s*:\s*"+?(|({service_name}[^"]+))"+\s*[,\]\}]"""
  """"awsRegion"\s*:\s*"({region}[^"]+)""""
  """"eventTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""
  """"eventName"+\s*:\s*"+?(|({operation}[^"]+))"+\s*[,\]\}]"""
  """"userIdentity":\{("[^,]+,)*"principalId\\?"+\s*:\s*\\?"+?({principal_id}[^"]+?)\\?"+\s*[,\]\}]"""
  """"sourceIPAddress":"(\s*|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
  """"bucket":[^\}\]]*"name":"({s3_bucket_name}[^"]+)"""
  """"userIdentity":\{("[^,]+,)*"arn"\\?:\s*\\?"({user_arn}[^"]+?)\\?""""
  """"+object.+?key\\?":\s*\\?"({file_path}.*?[\\\/]*({file_name}[^\\\/]+?))\s*""""
  """"size":({bytes}\d+)"""
  ]
 

}
```