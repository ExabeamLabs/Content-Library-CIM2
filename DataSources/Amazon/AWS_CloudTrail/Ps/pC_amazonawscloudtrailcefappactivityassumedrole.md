#### Parser Content
```Java
{
Name = amazon-awscloudtrail-cef-app-activity-assumedrole
  ParserVersion = "v1.0.0"
  Product = AWS CloudTrail
  Conditions = [  """AwsApiCall""", """eventName""", """awsRegion""", """type=AssumedRole""" ]
  Fields = ${AmazonParsersTemplates.s-aws-cloudtrail-activity-json.Fields}[
    """\Wsuser=[^=]*?({user}[^\\\/@=]+)@[^=]+?(\s+\w+=|\s*$)""",
    #"""\Wext_userIdentity_sessionContext_sessionIssuer_type=(|({operation}.+?))(\s+\w+=|\s*$)""",
    """"userIdentity".*?"sessionContext".*?"sessionIssuer".*?"type":"({operation}[^"]+)"""",
    """\WflexString1=(|({operation}[^=]+?))(\s+\w+=|\s*$)""",
    """"+userName"+\s*:\s*"+?(|({target}[^"]+?))"+\s*[,\]\}]""",
    """"requestParameters":\{"userName":"({target}[^"]+)"\
s-aws-cloudtrail-activity-json = {
  Vendor = Amazon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"+eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z?)"+\s*[,\]\}]""",
    """"+sourceIPAddress"+\s*:\s*"+?(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^"].+?))"+\s*[,\]\}]""",
    """"+eventSource"+\s*:\s*"+?(|({host}[^"]+?))"+\s*[,\]\}]""",
    """"userIdentity".+?"+invokedBy"+\s*:\s*"+?(|({dest_host}[^"].+?))"+\s*[,\]\}]""",
    """({app}AwsApiCall)""",
    """"+eventName"+\s*:\s*"+?(|({action}[^"].+?))"+\s*[,\]\}]""",
    """"+eventName"+\s*:\s*"+?(|({operation}[^"].+?))"+\s*[,\]\}]""",
    """"userIdentity\\?".+?"arn\\?"\s*:\s*\\?"?(|arn:aws:sts::\d+:[^\/]+\/({user}[^"]+)\/+(?!\-\d+)[^\/]+?)(@[\w\.]+)?\\?"\s*[,\]\}]""",
    """"+userName"+\s*:\s*"+?(|({user}[^"].+?))"+\s*[,\]\}]""",
    """"eventSource"\s*:\s*"(|({service_name}[^"]+))"""",
    """"sessionIssuer"\s*:\s*.*?"arn"\s*:\s*"(?:|({object}[^"]+))"""",
    """"bucketName"\s*:\s*"(|({bucket_name}[^"]+))"""",
    """"policyArn"\s*:\s*"(|({object}[^"]+))"""",
    """"roleName"\s*:\s*"(|({object}[^"]+))"""",
    """"userAgent"\s*:\s*"\[?(|({user_agent}[^"]+?))\]?"""",
    """"+errorCode"+\s*:\s*"+?(|({activity_outcome}[^"]+?))"+\s*[,\]\}]""",
    """"+errorMessage"+\s*:\s*"+?(|({additional_info}[^"]+?))"+\s*[,\]\}]""",
    """"+accountId"+\s*:\s*"+?(|({account_id}[^"]+?))"+\s*[,\]\}]""",
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
    """items":\[[^\]]+?ipProtocol":"({protocol}[^"]+)""""
  
}
```