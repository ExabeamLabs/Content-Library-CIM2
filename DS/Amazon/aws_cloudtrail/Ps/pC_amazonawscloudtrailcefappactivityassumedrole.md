#### Parser Content
```Java
{
Name = amazon-awscloudtrail-cef-app-activity-assumedrole
  Vendor = Amazon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ParserVersion = "v1.0.0"
  Product = AWS CloudTrail
  Conditions = [  """AwsApiCall""", """eventName""", """awsRegion""", """type=AssumedRole""" ]
  Fields = ${AwsParserTemplates.aws-cloudtrail-user-template.Fields}[
    """"+eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z?)"+\s*[,\]\}]""",
    """"+sourceIPAddress"+\s*:\s*"+?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^"].+?))"+\s*[,\]\}]""",
    """"+eventSource"+\s*:\s*"+?(|({host}[^"]+?))"+\s*[,\]\}]""",
    """"userIdentity".+?"+invokedBy"+\s*:\s*"+?(|({dest_host}[^"].+?))"+\s*[,\]\}]""",
    """({app}AwsApiCall)""",
    """"+eventName"+\s*:\s*"+?(|({action}[^"].+?))"+\s*[,\]\}]""",
    """"+eventName"+\s*:\s*"+?(|({operation}[^"].+?))"+\s*[,\]\}]""",
    """"eventSource"\s*:\s*"(|({service_name}[^"]+))"""",
    """"sessionIssuer"\s*:\s*.*?"arn"\s*:\s*"(?:|({object}[^"]+))"""",
    """"bucketName"\s*:\s*"(|({bucket_name}[^"]+))"""",
    """"policyArn"\s*:\s*"(|({object}[^"]+))"""",
    """"roleName"\s*:\s*"(|({role}[^"]+))"""",
    """"userAgent"\s*:\s*"\[?(|({user_agent}[^"]+?))\]?"""",
    """"+errorCode"+\s*:\s*"+?(|({result}[^"]+?))"+\s*[,\]\}]""",
    """"+errorMessage"+\s*:\s*"+?(|({additional_info}[^"]+?))"+\s*[,\]\}]""",
    """"+accountId"+\s*:\s*"+?(|({resource}[^"].+?))"+\s*[,\]\}]""",
    """"requestParameters"\s*:[^\}]+?"instanceId"\s*:\s*"({request_id}[^"]+)",("attribute"\s*:\s*"({request_action}[^"]+)")?""",
    """"awsRegion"\s*:\s*"({region}[^"]+)"""",
    #"""ext_userIdentity_type=({user_type}.+?)\s*\w+=""",
    """"userIdentity".*?"type":"({user_type}[^"]+?)"""",
    """userIdentity.+?type\\?":\s*\\?"({user_type}[^"]+?)\\?"""",
    """assumed-role"[^:]+?:role\/({role}[^"]+)""",
    """bytesTransferredOut":\s*({bytes_out}\d+(\.\d+)?)"""
    """bytesTransferredIn":\s*({bytes_in}\d+(\.\d+)?)""",
    """\srequestClientApplication=({app}[^\s]+)\s""",
    """items":\[[^\]]+?fromPort":({src_port}\d+),"""",
    """items":\[[^\]]+?toPort":({dest_port}\d+),"""",
    """items":\[[^\]]+?ipProtocol":"({protocol}[^"]+)"""",
    #"""\Wext_userIdentity_sessionContext_sessionIssuer_type=(|({operation}.+?))(\s+\w+=|\s*$)""",
    """"userIdentity".*?"sessionContext".*?"sessionIssuer".*?"type":"({operation}[^"]+)"""",
    """\WflexString1=(|({operation}[^=]+?))(\s+\w+=|\s*$)""",
    """"+userName"+\s*:\s*"+?(|({target}[^"]+?))"+\s*[,\]\}]""",
    """"requestParameters":\{"userName":"({target}[^"]+)"\},""",
    """"sessionIssuer"\s*:\s*[^@]*?"arn":"[^"]*?role/({role}[^"\\\/]+)""",
    """requestParameters"+:.+?"+instanceId"+:"+({request_id}[^"]+)","attribute":"({request_action}[^"]+)"""",
    """\sresource:\s+({additional_info}[^\s"]+)(\s|")""",
    """"responseElements":[^@]+?"name":"({object_name}[^"]+)"""",
    """"responseElements":[^@]+?"s3BucketName":"({object}[^"]+)"""",
    """"responseElements":[^@]+?"s3KeyPrefix":"({object_key_prefix}[^"]+)"""",
    """"responseElements":[^@]+?"snsTopicName":"({sns_topic_name}[^"]+)"""",
    """"awsRegion":"({region}[^"]+)"""",
    """\srequestClientApplication=({app}[^\s]+)\s""",
    """"policyName":"({policy_name}[^"]+)"""",
    """"configRuleName":"({rule}[^"]+)""""
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