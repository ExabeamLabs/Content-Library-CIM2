#### Parser Content
```Java
{
Name = amazon-awscloudtrail-cef-app-activity-assumedrole
  Vendor = Amazon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ParserVersion = "v1.0.0"
  Product = AWS CloudTrail
  Conditions = [  """AwsApiCall""", """eventName""", """awsRegion""", """type=AssumedRole""" ]
  Fields = [
    """"+eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z?)"+\s*[,\]\}]""",
    """"+sourceIPAddress"+\s*:\s*"+?(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^"].+?))"+\s*[,\]\}]""",
    """"+eventSource"+\s*:\s*"+?(|({host}[^"]+?))"+\s*[,\]\}]""",
    """"userIdentity".+?"+invokedBy"+\s*:\s*"+?(|({dest_host}[^"].+?))"+\s*[,\]\}]""",
    """({app}AwsApiCall)""",
    """"+eventName"+\s*:\s*"+?(|({action}[^"].+?))"+\s*[,\]\}]""",
    """"+eventName"+\s*:\s*"+?(|({operation}[^"].+?))"+\s*[,\]\}]""",
    """"userIdentity\\?".+?"arn\\?"\s*:\s*\\?"?(|arn:aws:sts::\d+:[^\/]+\/((\w+\-){6}\w+|({user}[^"]+))\/+(?!\-\d+)[^\/]+?)(@[\w\.]+)?\\?"\s*[,\]\}]""",
    """"+userName"+\s*:\s*"+?(|(\w+\-){6}\w+|({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[^"].+?))"+\s*[,\]\}]""",
    """"eventSource"\s*:\s*"(|({service_name}[^"]+))"""",
    """"sessionIssuer"\s*:\s*.*?"arn"\s*:\s*"(?:|({object}[^"]+))"""",
    """"bucketName"\s*:\s*"(|({bucket_name}[^"]+))"""",
    """"policyArn"\s*:\s*"(|({object}[^"]+))"""",
    """"roleName"\s*:\s*"(|({object}[^"]+))"""",
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
    """"userIdentity\\?".+?"arn\\?"\s*:\s*\\?"?arn:aws:iam::[^\/"]+\/(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+))"""
    """"userIdentity\\?".+?"arn\\?"\s*:\s*\\?"?arn:aws:sts::\d+:assumed-role\/([^\/"]+\/)(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+))"""
    """"{1,20}userIdentity\\?".+?"arn\\?"\s*:\s*\\?"?arn:aws:sts::\d+:assumed-role\/([^\/"]+\/)(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+)(@({domain}[^@"\.]+)))\\?"+\s*[,\]\\\\\}]"""
    """\Wsuser=[^=]*?(({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?)|({user}[^\\\/@=]+)@[^=]+?)(\s+\w+=|\s*$)""",
    #"""\Wext_userIdentity_sessionContext_sessionIssuer_type=(|({operation}.+?))(\s+\w+=|\s*$)""",
    """"userIdentity".*?"sessionContext".*?"sessionIssuer".*?"type":"({operation}[^"]+)"""",
    """\WflexString1=(|({operation}[^=]+?))(\s+\w+=|\s*$)""",
    """"+userName"+\s*:\s*"+?(|({target}[^"]+?))"+\s*[,\]\}]""",
    """"requestParameters":\{"userName":"({target}[^"]+)"\},""",
    """"sessionIssuer"\s*:\s*[^@]*?"arn":"[^"]*?role/({role}[^"\\\/]+)""",
    """"UserId":\s"({email_address}[^@"]+@({email_domain}[^"\.]+\.[^"]+))"""
    """requestParameters"+:.+?"+instanceId"+:"+({request_id}[^"]+)","attribute":"({request_action}[^"]+)"""",
    """\sresource:\s+({additional_info}[^\s"]+)(\s|")""",
    """"responseElements":[^@]+?"name":"({object_name}[^"]+)"""",
    """"responseElements":[^@]+?"s3BucketName":"({object}[^"]+)"""",
    """"responseElements":[^@]+?"s3KeyPrefix":"({object_key_prefix}[^"]+)"""",
    """"responseElements":[^@]+?"snsTopicName":"({sns_topic_name}[^"]+)"""",
    """"awsRegion":"({region}[^"]+)"""",
    """\srequestClientApplication=({app}[^\s]+)\s""",
    """"policyName":"({policy_name}[^"]+)"""",
    """"configRuleName":"({rule}[^"]+)"""",
  ]


}
```