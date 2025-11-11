#### Parser Content
```Java
{
Name = microsoft-o365-kv-file-write-success-anonymouslinkcreated
Conditions = [
  """SESSID="""
  """RESULTCODE="""
  """WORKLOAD="""
  """COMMAND=AnonymousLinkCreated"""
  """ITEMTYPE=File"""
  """OBJECT="""
]
ParserVersion = "v1.0.0"

logrhythm-o365-file-operation = {
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """\sTS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """USER=(Unknown|({email_address}[^@\s]+@[^\s\.]+?\.[^\s]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s]+))?)\s+\w+=""",
    """DOMAIN=(|({domain}[^\s]+?))\s+\w+=""",
    """USER=({domain}[^\\\s]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """WORKLOAD=({app}[^=]+?)\s+\w+=""",
    """COMMAND=({operation}({event_name}[^=]+?))\s+\w+=""",
    """OBJECT=({file_path}({object}[^=]+?))\s+\w+=""",
    """\sFILENAME=({file_name}[^=]+?(\.({file_ext}[^\s\=\.]+))?)\s+\w+=""",
    """SIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """USERAGENT=\s*(|({user_agent}[^\n]+?))\s*(\w+=|$)""",
    """ITEMTYPE=({file_type}[^=]+?)\s+\w+="""
    ]
 },

azure-app-activity-skyfromation= {
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)\s+[^\s]+\s+""",
    """"+src-event-id"+:"+({event_code}[^"]+)""",
    """"+event-name"+:"+({event_name}[^"]+)""",
    """"+application-module"+:"+({app_module}[^"]+)""",
    """"+authorization"+:.+?action"+:"+({action}[^"]+)""",
    """"+authorization"+:.+?scope"+:"+({scope}[^"]+)""",
    """"caller"+:"+((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
    """"channels"+:"+({channels}[^"]+)""",
    """"claims".+?aud"+:"+({aud}[^"]+)""",
    """"claims".+?iss"+:"+({iss}[^"]+)""",
    """"claims".+?iat"+:"+({iat}[^"]+)""",
    """"claims".+?nbf"+:"+({nbf}[^"]+)""",
    """"claims".+?exp"+:"+({exp}[^"]+)""",
    """"claims".+?aio"+:"+({aio}[^"]+)""",
    """"claims".+?appid"+:"+({app_id}[^"]+)""",
    """"claims".+?appidacr"+:"+({app_id_acr}[^"]+)""",
    """"+uti"+:"+({uti}[^"]+)""",
    """"+ver"+:"+({version}[^"]+)""",
    """"+xms_mirid"+:"+({xms_mirid}[^"]+)""",
    """"+correlationId"+:"+({correlation_id}[^"]+)""",
    """"+description"+:"+({additional_info}[^",]+)""",
    """"+httpRequest".+?clientRequestId":"({user_id}[^"]+)""",
    """"+httpRequest".+?clientIpAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"+httpRequest".+?method"+:"+({method}[^"]+)""",
    """"+properties.+?statusCode"+:"+({result}[^"]+)""",
    """"+properties.+?serviceRequestId"+:"+({service_request_id}[^"]+)""",
    """"+properties.+?statusMessage".+?error.+?code\\*"+:\\+"+({error_code}[^\\]+)""",
    # error_msg is removed
    """"+category"+:"+({category}[^"]+)"""
    """"+subscriptionId"+:"+({subscription_id}[^"]+)""",
    """"+tenantId"+:"+({tenant_id}[^"]+)"""
    """"+provider-account-identifier".+?id"+:"+({account_id}[^"]+)""",
    """"+provider-account-identifier".+?name"+:"+({resource}[^"]+)"""
    """"+type"+:"+({object}[^"]+)""",
    """"+src-application-name"+:"+({app}[^"]+)""",
    """"+src-account-name"+:"+({account_name}[^"]+)""",
    """"+src-account-id"+:"+({account_id}[^"]+)"""
    """"+src-endpoint"+:"+({endpoint}[^"]+)""",
    """operationName"+:\s*\{[^\}]*?"+localizedValue"+:\s*"+({operation}[^"]+)""",  
    """exa_json_path=$.subscriptionId,exa_field_name=subscription_id"""
    """exa_json_path=$.operationName.localizedValue,exa_field_name=operation"""
    """"(r|R)esourceId":\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)\/[^"]+)""""
    """exa_regex=(r|R)esourceId":\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)\/[^"]+)""""

}
```