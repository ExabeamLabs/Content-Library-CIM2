#### Parser Content
```Java
{
Name = "amazon-awscloudtrail-json-app-login-awsconsolesignin"
ParserVersion = v1.0.0
Vendor = "Amazon"
Product = "AWS CloudTrail"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""AwsConsoleSignIn"""
"""eventName"""
]
Fields = [
""""+eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z)"+\s*[,\]\}]"""
""""+sourceIPAddress"+\s*:\s*"+?(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"+\s*[,\]\}]"""
""""+eventName"+\s*:\s*"+?(|({action}[^"].+?))"+\s*[,\]\}]"""
""""+eventSource"+\s*:\s*"+?(|({host}[^"].+?))"+\s*[,\]\}]"""
""""+userName"+\s*:\s*"+?(|({user}[^"].+?))"+\s*[,\]\}]""",
""""userIdentity\\?".+?"arn\\?"\s*:\s*\\?"?arn:aws:iam::[^\/"]+\/(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+))"""
""""userIdentity\\?".+?"arn\\?"\s*:\s*\\?"?arn:aws:sts::\d+:assumed-role\/([^\/"]+\/)(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+))"""
""""errorMessage"\s*:\s*"({failure_reason}[^"]+)""""
""""responseElements\\?"\s*:\s*.+?\s*\\?".+?\\?"\s*:\s*\\?"({result}[^"]+?)\\?""""
""""eventType"+\s*:\s*"({app}[^"]+)""""
""""userAgent"+\s*:\s*"({user_agent}[^"]+)""""
""""recipientAccountId"+\s*:\s*"({object}[^"]+)""""
""""awsRegion":"({region}[^"]+)""""
"""\srequestClientApplication=({app}[^\s]+)\s"""
""""+requestParameters":\{("[^,]+,)*"roleSessionName\\?":\s*\\?"({session_name}[^"]+?)\\?"""",
""""+responseElements":\{"assumedRoleUser":\{("[^,]+,)*"assumedRoleId\\?":\s*\\?"({assumedRoleId}[^"]+?)\\?"""",
""""credentials":\{"accessKeyId":"({accessKeyId}[^"]+?)\\?""""
]


}
```