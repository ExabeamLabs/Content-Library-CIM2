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
    """CLIENT_IP="?({src_ip}[A-Fa-f:\d.]+)""",
    """Username="?({email}[^"\s,@]+@[^"\s,]+)""",
    """USER_ID="?({user}[^"\s,]+)""",
    """REQUEST_SIZE="?({bytes}\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```