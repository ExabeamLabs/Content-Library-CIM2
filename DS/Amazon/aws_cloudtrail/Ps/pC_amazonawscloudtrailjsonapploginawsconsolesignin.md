#### Parser Content
```Java
{
Name = "amazon-awscloudtrail-json-app-login-awsconsolesignin"
ParserVersion = v1.0.0
Vendor = "Amazon"
Product = "AWS CloudTrail"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""AwsConsoleSignIn"""
"""eventName"""
]
Fields = ${AwsParserTemplates.aws-cloudtrail-user-template.Fields}[
""""+eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ?))"+\s*[,\]\}]"""
""""+sourceIPAddress"+\s*:\s*"+?(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"+\s*[,\]\}]"""
""""+eventName"+\s*:\s*"+?(|({operation}[^"].+?))"+\s*[,\]\}]"""
""""+eventSource"+\s*:\s*"+?(|({host}[^"].+?))"+\s*[,\]\}]"""
""""errorMessage"\s*:\s*"({failure_reason}[^"]+)""""
"""responseElements\\?"\s*:\s*"?\{.*?\\?"(ConsoleLogin|CheckMfa|GetSigninToken|RenewRole)\\?":\\?\s*"({result}[^"\\]+?)\\?""""
""""eventType"+\s*:\s*"({app}[^"]+)""""
""""userAgent"+\s*:\s*"({user_agent}[^"]+)""""
""""recipientAccountId"+\s*:\s*"({additional_info}[^"]+)""""
""""awsRegion":"({region}[^"]+)""""
"""\srequestClientApplication=({app}[^\s]+)\s"""
""""+requestParameters":\{("[^,]+,)*"roleSessionName\\?":\s*\\?"({session_name}[^"]+?)\\?"""",
""""+responseElements":\{"assumedRoleUser":\{("[^,]+,)*"assumedRoleId\\?":\s*\\?"({assumedRoleId}[^"]+?)\\?"""",
""""credentials":\{"accessKeyId":"({key_id}[^"]+?)\\?""""
""""accessKeyId":"({key_id}[^"]+?)""""
"""exa_json_path=$.userIdentity.userName,exa_regex=(({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
"""exa_json_path=$.eventTime,exa_field_name=time""",
"""exa_json_path=$.sourceIPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$.eventName,exa_field_name=operation""",
"""exa_json_path=$.eventSource,exa_field_name=host""",
"""exa_json_path=$.errorMessage,exa_field_name=failure_reason""",
"""exa_json_path=$.eventType,exa_field_name=app""",
"""exa_json_path=$.userAgent,exa_field_name=user_agent""",
"""exa_json_path=$.awsRegion,exa_field_name=region""",
"""exa_json_path=$.userIdentity.accessKeyId,exa_field_name=key_id""",
"""exa_json_path=$..recipientAccountId,exa_field_name=additional_info""",
"""exa_json_path=$..responseElements,exa_regex="(ConsoleLogin|CheckMfa|GetSigninToken|RenewRole)\\?":\\?\s*"({result}[^"\\]+?)\\?"""",
"""exa_json_path=$.recipientAccountId,exa_field_name=aws_account"""
]

aws-cloudtrail-user-template = {
    Fields = [
      """\Wsuser=[^=]*?(({aws_email_address}({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@[^=]+?)?)(\s+\w+=|\s*$)""",
      """\\?"type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":.+?"arn\\?":\s*\\?"arn:aws:sts::\d+:assumed-role\/({role}[^\/"]+)\/(AssumeRoleSession|((?![\w\-\.]{30,})(({aws_email_address}[^"@]+@[^"\.]+\.[^"]+)|({aws_account}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?"""",
      """"sourceIdentity\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":.+?"AssumedRole\\?".+?"principalId\\?":\s*\\?"[A-Z\d]{1,25}:({aws_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"""",
      ""","userIdentity\\?":.+?,"AssumedRole\\?".+?,"sessionIssuer\\?":\s*\{[^\}]+?,"IAMUser\\?"[^\}]+?,"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":.+?"IAMUser\\?".+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":\s*\{.*?"type\\?":\s*\\?"({aws_account}({user}Root))\\?""""
      """exa_regex=\Wsuser=[^=]*?(({aws_email_address}({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@[^=]+?)?)(\s+\w+=|\s*$)""",
      """exa_regex=\\?"type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """exa_regex="userIdentity\\?":.+?"arn\\?":\s*\\?"arn:aws:sts::\d+:assumed-role\/({role}[^\/"]+)\/(AssumeRoleSession|((?![\w\-\.]{30,})(({aws_email_address}[^"@]+@[^"\.]+\.[^"]+)|({aws_account}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?"""",
      """exa_regex="sourceIdentity\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """exa_regex="userIdentity\\?":.+?"AssumedRole\\?".+?"principalId\\?":\s*\\?"[A-Z\d]{1,25}:({aws_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"""",
      """exa_regex="userIdentity\\?":.+?,"AssumedRole\\?".+?,"sessionIssuer\\?":\s*\{[^\}]+?,"IAMUser\\?"[^\}]+?,"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """exa_regex="userIdentity\\?":.+?"IAMUser\\?".+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """exa_regex="userIdentity\\?":\s*\{.*?"type\\?":\s*\\?"({aws_account}({user}Root))\\?""""
    
}
```