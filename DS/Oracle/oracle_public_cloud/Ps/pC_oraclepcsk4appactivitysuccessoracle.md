#### Parser Content
```Java
{
Name = oracle-pc-sk4-app-activity-success-oracle
  Vendor = Oracle
  Product = Oracle Public Cloud
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ CEF:""", """"oracle":""", """"compartmentId":"""", """"type":"com.oraclecloud.objectstorage""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """"clientIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"type":"com.oraclecloud.objectstorage.({operation}[^"]+)"""",
    """"bucketName":"({bucket_name}[^"]+)"""",
    """({service_name}objectstorage)""",
    """"userAgent":"({user_agent}[^"]+)"""",
    """"requestAction":"({method}[^"]+)"""",
    """"action":"({method}[^"]+)"""",
    """"statusCode":({result_code}\d+)""",
    """"objectName":"({object}[^"]+)"""",
    """"message":"({additional_info}[^"]+)"""",
  ]


}
```