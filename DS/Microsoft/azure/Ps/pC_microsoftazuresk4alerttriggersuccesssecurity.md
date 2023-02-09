#### Parser Content
```Java
{
Name = microsoft-azure-sk4-alert-trigger-success-security
  ParserVersion = v1.0.0
  Conditions = [ """"category":"Security"""", """"eventName"""", """EventHub""" ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-event-hub-1.Fields}[
    """compromisedEntity":"({user_upn}[^"]+)"""",
    """userName":"(({domain}[^\\"]+)\\+)?({user}[^"]+)"""",
    """clientIPAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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
Product = Azure
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z [\w\-.]+ """
"""\"time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""\Wdvc=({host}\S+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wact=({operation}[^=]+)\s+(\w+=|$)"""
"""([^\|]*\|){5}({operation}[^\|]+)"""
"""\WflexString1=({operation}[^=]+)\s+(\w+=|$)"""
"""\WdestinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
"""\Wfname=({object}[^=]+)\s+(\w+=|$)"""
"""\Wmsg=({additional_info}[^=]+)\s+(\w+=|$)"""
"""\Wduser=(anonymous|({email_address}[^@=]+@[^@=]+?)|({user}.+?))(\s+\w+=|\s*$)"""
"""\Wsuser=(anonymous|({email_address}[^@=]+@[^@=\s]+)|({user}[^\s]+))(\s+|\s*$)"""
"""\Wsuid=(anonymous|({email_address}[^@=]+@[^@=]+?)|({user}.+?))(\s+\w+=|\s*$)"""
"""\Woutcome=({result}[^=]+)\s+(\w+=|$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wshost=(|--|({src_host}[^=]+))(\s+\w+=|\s*$)"""
"""\"clientIP\":\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"description\":\"({additional_info}[^\"]+)"""
"""\"identity\".*?\"claims\".*?\"name\":\"({user}[^\"]+)\""""
"""\"callerIpAddress\":\"({src_ip}[a-fA-F\d.:]+)\""""
"""Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]"""
"""EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
"""\[Namespace:\s*({host}\S+) ; EventHub name:"""
"""\"host_name\":\"({host}[^\"]+)\""""

}
```