#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-app-activity-success-getrolecredentials
	ParserVersion = v1.0.0
	Conditions = [ """"destinationServiceName":"AWS"""", """"dproc":"CloudTrail"""", """"eventName":"GetRoleCredentials"""", """"eventType":"AwsServiceEvent"""" ]
	Fields = ${AwsParserTemplates.aws-cloudtrail-json-2.Fields}[
	""""account_id":"({account_id}[^"]+)"""
	""""sourceIPAddress":"(\s*|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
	""""userAgent":"(\s*|({user_agent}[^"]+))"""",
	""""userName":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""""
	""""readOnly"\s*:\s*({readonly}[^",\}]+)("|,|\}\s*$)"""
	]

aws-cloudtrail-json-2 = {
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
  """"eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ?))"+\s*[,\]\}]""",
  """"destinationServiceName":"({app}[^"]+)"""",
  """"eventSource":"(\s*|({src_host}[^"]+))"""",
  """"eventName":"({event_name}[^"]+)"""",
  """"eventType":"({event_category}[^"]+)"""",
  """"eventID":"({alert_id}[^"]+)""",
  """"awsRegion"\s*:\s*"({region}[^"]+)"""",
  """"eventCategory":\s*"({event_category}[^"]+)""""
  
}
```