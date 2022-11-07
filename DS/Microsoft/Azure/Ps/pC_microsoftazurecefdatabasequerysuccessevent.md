#### Parser Content
```Java
{
Name = microsoft-azure-cef-database-query-success-event
ParserVersion = v1.0.0
Conditions = [
"""destinationServiceName =Azure"""
""""category":"SQLSecurityAuditEvents""""
""""database_name":""""
]
Fields = ${MicrosoftAzureParsersTemplates.cef-azure-event-hub-1.Fields}[
"""\"application_name\":\"({app}[^\"]+)\""""
"""\"statement\":\"({db_query}[^\"]+)\""""
"""\"database_name\":\"({db_name}[^\"]+)\""""
"""\"schema_name\":\"({db_schema}[^\"]+)\""""
"""\"server_principal_name\":\"({server_group}[^\"]+)\""""
"""\"client_ip\":\"({src_ip}[A-Fa-f\d\.:]+)\""""
"""\"additional_information\":\"({additional_info}[^\"]+)\""""
]  

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
"""\Wsrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\Wshost=(|--|({src_host}[^=]+))(\s+\w+=|\s*$)"""
"""\"clientIP\":\"({src_ip}[A-Fa-f.\d]+)"""
"""\"description\":\"({additional_info}[^\"]+)"""
"""\"identity\".*?\"claims\".*?\"name\":\"({user}[^\"]+)\""""
"""\"callerIpAddress\":\"({src_ip}[a-fA-F\d.:]+)\""""
"""Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]"""
"""EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
"""\[Namespace:\s*({host}\S+) ; EventHub name:"""
"""\"host_name\":\"({host}[^\"]+)\""""

}
```