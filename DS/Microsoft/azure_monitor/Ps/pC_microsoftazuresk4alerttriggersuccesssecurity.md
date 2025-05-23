#### Parser Content
```Java
{
Name = microsoft-azure-sk4-alert-trigger-success-security
  ParserVersion = v1.0.0
  Conditions = [ """"category":"Security"""", """"eventName"""", """"operationName":"""" ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-event-hub-1.Fields}[
    """"compromisedHost":"({dest_host}[\w\-.]+)"""",
    """compromisedEntity":"({user_upn}[^"]+)"""",
    """userName":"(({domain}[^\\"]+)\\+)?(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\(]+)\s*)""",
    """clientIPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """severity":"({alert_severity}[^"]+)"""",
    """operationId":"({alert_id}[^"]+)"""",
    """category":"({azure_category}[^"]+)"""",
    """attackedResourceType":"({azure_resource_type}[^"]+)"""",
    """eventName":"({alert_type}[^"\\]+)[\\]*"""",
    """"(detail|result)Description":"({additional_info}[^"]+)[\\]*"""",
    """"resourceId":"({resource}[^"]+)"""",
    """"resourceId":"[^"]*\/RESOURCEGROUPS\/({account_id}[^\/]+)\/""",
    """"correlationId":"({correlation_id}[^"]+)"""",
    """"operationName":"({operation}[^"]+)""""
  ]
  DupFields = ["alert_type->alert_name"]

cef-azure-event-hub-1 = {
Vendor = Microsoft
Product = Azure Monitor
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ" ]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """
"""\"time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""\Wdvc=({host}\S+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wact=({operation}[^=]+)\s+(\w+=|$)"""
"""([^\|]*\|){5}({operation}[^\|]+)"""
"""\WflexString1=({operation}[^=]+)\s+(\w+=|$)"""
"""destinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
"""\Wfname=({object}[^=]+)\s+(\w+=|$)"""
"""\Wmsg=({additional_info}[^=]+)\s+(\w+=|$)"""
"""\Wduser=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""\Wsuser=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+|\s*$)"""
"""\Wsuid=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""\Woutcome=({result}[^=]+)\s+(\w+=|$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wshost=(|--|({src_host}[^=]+))(\s+\w+=|\s*$)"""
"""\"clientIP\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"description\":\"({additional_info}[^\"]+)"""
"""\"identity\".*?\"claims\".*?\"name\":\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
"""\"callerIpAddress\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]"""
"""EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
"""\[Namespace:\s*({host}\S+) ; EventHub name:"""
"""\"host_name\":\"({host}[^\"]+)\""""
""""action_name":"({action}[^"]+)""""
""""LogicalServerName":"({server}[^"]+)"""
""""SubscriptionId":"({subscription_id}[^"]+)""""
""""ResourceGroup":"({resource_group}[^"]+)""""
""""resourceId":"({resource_id}[^"]+)""""
""""level"\s*:\s*"({severity}[^",]+)""",
""""resourceId":"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?\/[^"]+)""""

}
```