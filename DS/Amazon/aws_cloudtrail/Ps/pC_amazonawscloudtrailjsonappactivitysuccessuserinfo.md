#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-app-activity-success-userinfo
  ParserVersion = v1.0.0
  Conditions = [ """"destinationServiceName":"AWS"""", """"dproc":"CloudTrail"""", """"eventName":"UserInfo_GET"""", """"eventType":"AwsServiceEvent"""" ]
  Fields = ${DLAwsParserTemplates.aws-cloudtrail-json-1.Fields}[
    """"userPoolDomain":"({domain}[^"]+)"""",
    """"userPoolId":"({user_id}[^"]+)"""",
    """"serviceAccountId":"({service_id}[^"]+)"""",
    """"status":({result_code}\d+)"""
  ]

aws-cloudtrail-json-1 = {
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """"eventTime":"({time}\d\d\d\d-\d\d-\d\dT11:11:11Z)"""",
	  """"destinationServiceName":"({app}[^"]+)"""",
	  """"awsAccountId":"({account_id}[^"]+)"""",
	  """"userIdentity":.*?"accountId":"({account_id}[^"]+)"""",
	  """"sourceIPAddress":"(\s*|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
	  """"eventSource":"(\s*|({src_host}[^"]+))"""",
	  """"userAgent":"(\s*|({user_agent}[^"]+))"""",
	  """"eventType":"({event_category}[^"]+)"""",
	  """"eventName":"({event_name}[^"]+)"""",
	  """"userName":"({user}[\w\.\-]{1,40}\$?)""""
  
}
```