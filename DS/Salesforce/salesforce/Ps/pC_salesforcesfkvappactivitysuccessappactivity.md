#### Parser Content
```Java
{
Name = salesforce-sf-kv-app-activity-success-appactivity
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """SFDCLogType=""", """SFDCLogId=""" ]
  Fields = [
    """SFDCLogDate="({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d.\d\d\d(\-|\+)\d+)""",
    """PAGE_NAME="?({object}[^",]+)""",
    """ENTITY_NAME="?({object}[^",]+)""",
    """object="?({object}[^",]+)""",
    """METHOD_NAME="?({operation}[^",]+)""",
    """action="?({operation}[^",]+)""",
    """CLIENT_NAME="?({user_agent}[^",]+)""",
    """CLIENT_IP="?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Username="?({email_address}[^"\s,@]+@[^"\s,]+)""",
    """USER_ID="?({user}[^"\s,]+)""",
    """REQUEST_SIZE="?({bytes}\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```