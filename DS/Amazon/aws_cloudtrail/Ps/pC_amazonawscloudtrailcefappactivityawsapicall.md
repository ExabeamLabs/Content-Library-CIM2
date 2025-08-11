#### Parser Content
```Java
{
Name = amazon-awscloudtrail-cef-app-activity-awsapicall
  Vendor = Amazon
  Product = AWS CloudTrail
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [  """AwsApiCall""", """eventName""", """awsRegion""" ]
  Fields = ${AwsParserTemplates.aws-cloudtrail-user-template.Fields}[
    """"userIdentity":\{("[^,]+,)*"type"\\?:\s*\\?"({user_type}[^"]+?)\\?"""",
    """"userIdentity":\{("[^,]+,)*"arn"\\?:\s*\\?"({user_arn}[^"]+?)\\?"""",
    """"userIdentity":\{("[^,]+,)*"accountId\\?"+\s*:\s*\\?"+?({aws_account}[^"]+?)\\?"+\s*[,\]\}]""",
    """"userIdentity":\{("[^,]+,)*"principalId\\?"+\s*:\s*\\?"+?({principal_id}[^"]+?)\\?"+\s*[,\]\}]""",
    """"userIdentity":\{("[^,]+,)*"attributes":\{("[^,]+,)*"mfaAuthenticated"\\?:\s*\\?"({mfa}[^"]+?)\\?"""",
    """"assumedRoleUser":\{("[^,]+,)*"arn"\s*:\s*"({assumed_role_arn}[^"]+)\\?""""
    """"eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z?)"+\s*[,\]\}]""",
    """"eventSource"+\s*:\s*"+?(|({service_name}[^"]+))"+\s*[,\]\}]""",
    """"eventName"+\s*:\s*"+?(|({operation}[^"]+))"+\s*[,\]\}]""",
    """"awsRegion"\s*:\s*"({region}[^"]+)"""",
    """"sourceIPAddress"+\s*:\s*"+?(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^"]+))"+\s*[,\]\}]""",
    """"userAgent"\s*:\s*"\[?(|({user_agent}[^"]+?))\]?"""",
    """"eventID\\?"+:\\?"+({event_code}[^"\\]+)\\?"""",
    """"eventType"+\s*:\s*"+?(|({event_category}[^"]+))"+\s*[,\]\}]""",
    """"errorCode"\s*:\s*"({result}[^"]+)"""",
    """"errorMessage"\s*:\s*"({failure_reason}[^"]+)"""",
    """"readOnly"\s*:\s*({readonly}[^",\}]+)("|,|\}\s*$)""",
    """"vpcEndpointId":"({vpc}[^"]+)""",
    """"+requestParameters":\{("[^,]+,)*"roleSessionName\\?":\s*\\?"({session_name}[^"]+?)\\?"""",
    """"+responseElements":\{"assumedRoleUser":\{("[^,]+,)*"assumedRoleId\\?":\s*\\?"({assumedRoleId}[^"]+?)\\?"""",
    """"accessKeyId":"({key_id}[^"]+?)"""",
    """"requestParameters":"\{?[^\}]+"userName\\?":\\?"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^"\\]+))\\?""""
    """requestParameters":"({additional_info}.+?),"\w+"?:"""
  ]

aws-cloudtrail-user-template = {
    Fields = [
      """\Wsuser=[^=]*?(({aws_email_address}({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@[^=]+?)?)(\s+\w+=|\s*$)""",
      """\\?"type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":.+?"arn\\?":\s*\\?"arn:aws:sts::\d+:assumed-role\/({role}[^\/"]+)\/(AssumeRoleSession|((?![\w\-\.]{30,})(({aws_email_address}[^"@]+@[^"\.]+\.[^"]+)|({aws_account}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?"""",
      """"sourceIdentity\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":\{[^\}]+"AssumedRole\\?"[^\}]+"principalId\\?":\s*\\?"[A-Z\d]{1,25}:({aws_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"""",
      ""","userIdentity\\?":.+?"IAMUser\\?".+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":\s*\{"type\\?":\s*\\?"({aws_account}({user}Root))\\?""""
      """exa_regex=\Wsuser=[^=]*?(({aws_email_address}({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@[^=]+?)?)(\s+\w+=|\s*$)""",
      """exa_regex=\\?"type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """exa_regex="userIdentity\\?":.+?"arn\\?":\s*\\?"arn:aws:sts::\d+:assumed-role\/({role}[^\/"]+)\/(AssumeRoleSession|((?![\w\-\.]{30,})(({aws_email_address}[^"@]+@[^"\.]+\.[^"]+)|({aws_account}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?"""",
      """exa_regex="sourceIdentity\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """exa_regex="userIdentity\\?":\{[^\}]+"AssumedRole\\?"[^\}]+"principalId\\?":\s*\\?"[A-Z\d]{1,25}:({aws_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"""",
      """exa_regex="userIdentity\\?":.+?"IAMUser\\?".+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """exa_regex="userIdentity\\?":\s*\{"type\\?":\s*\\?"({aws_account}({user}Root))\\?""""
      """exa_regex=\WawsRegion":"({region}[^"]+)""""
      """"awsRegion"\s*:\s*"({region}[^"]+)""""
    
}
```