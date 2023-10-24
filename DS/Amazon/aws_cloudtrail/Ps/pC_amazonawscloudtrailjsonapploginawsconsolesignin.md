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
Fields = ${AwsParserTemplates.aws-cloudtrail-user-template.Fields}[
""""+eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z)"+\s*[,\]\}]"""
""""+sourceIPAddress"+\s*:\s*"+?(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"+\s*[,\]\}]"""
""""+eventName"+\s*:\s*"+?(|({action}[^"].+?))"+\s*[,\]\}]"""
""""+eventSource"+\s*:\s*"+?(|({host}[^"].+?))"+\s*[,\]\}]"""
""""errorMessage"\s*:\s*"({failure_reason}[^"]+)""""
""""responseElements\\?"\s*:\s*.+?\s*\\?".+?\\?"\s*:\s*\\?"({result}[^"]+?)\\?""""
""""eventType"+\s*:\s*"({app}[^"]+)""""
""""userAgent"+\s*:\s*"({user_agent}[^"]+)""""
""""recipientAccountId"+\s*:\s*"({additional_info}[^"]+)""""
""""awsRegion":"({region}[^"]+)""""
"""\srequestClientApplication=({app}[^\s]+)\s"""
""""+requestParameters":\{("[^,]+,)*"roleSessionName\\?":\s*\\?"({session_name}[^"]+?)\\?"""",
""""+responseElements":\{"assumedRoleUser":\{("[^,]+,)*"assumedRoleId\\?":\s*\\?"({assumedRoleId}[^"]+?)\\?"""",
""""credentials":\{"accessKeyId":"({accessKeyId}[^"]+?)\\?""""
]

aws-cloudtrail-user-template = {
    Fields = [
      """\Wsuser=[^=]*?(({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?)|({user}[\w\.\-]{1,40}\$?)(@[^=]+?)?)(\s+\w+=|\s*$)""",
      """\\?"type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"arn\\?":\s*\\?"arn:aws:sts::\d+:assumed-role\/([^\/"]+\/)(AssumeRoleSession|((?![\w\-\.]{30,})(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?"""",
      """"sourceIdentity\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"AssumedRole\\?".+?"principalId\\?":\s*\\?"[A-Z\d]{1,50}:({email_address}[^"]+?@[^@"]+)\\?"\s*[,\]\}]""",
      """"userIdentity\\?":.+?"AssumedRole\\?".+?"sessionIssuer\\?":\s*\{[^\}]+?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"IAMUser\\?".+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":\s*\{.*?"type\\?":\s*\\?"({user}Root)\\?""""
    
}
```