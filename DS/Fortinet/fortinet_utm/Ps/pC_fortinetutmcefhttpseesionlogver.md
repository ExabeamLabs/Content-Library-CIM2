#### Parser Content
```Java
{
Name = "fortinet-utm-cef-http-seesion-logver"
Vendor = "Fortinet"
Product = "Fortinet UTM"
TimeFormat = "epoch"
Conditions = [
"""ad.subtype="""
"""ad.eventtype="""
"""ad.direction="""
"""deviceExternalId="""
"""logver"""
]
Fields = [
"""\sad.eventtime=({time}\d{13})"""
"""\sdvchost=({host}[^\s]+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sspt=({src_port}\d+)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdpt=({dest_port}\d+)"""
"""\sact=({action}[^\s]+)"""
"""\sdhost=({web_domain}[^\s]+)"""
"""request=((\w+:\/+)?({web_domain}[^\s\/]+)({uri_path}\/[^\s\?]*)?({uri_query}\?[^\s]*)?)\s+[\w.]+="""
"""\sout=({bytes_out}\d+)"""
"""\sin=({bytes_in}\d+)"""
"""\smsg=({event_name}[^=]+?)\s+([\w.]+=|$)"""
"""\sact=blocked[^\n]+?msg=({result_reason}[^=]+?)\s+([\w.]+=|$)"""
"""\sproto=({protocol}[^\s]+)\s+\w+="""
"""\sad.direction=({direction}[^=]+?)\s+\w+="""
"""referralurl=({referrer}[^\s]+)"""
"""\sad.policyid=({policy_id}[^\s]+)"""
"""\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\sad.agent=({user_agent}[^=]+?)\s+[\w.]+="""
"""requestContext=({category}[^=]+?)\s+([\w.]+=|$)"""
"""deviceSeverity=({additional_info}[^=]+?)\s+([\w.]+=|$)""",
"""\sad\.profile=({profile}[^=]+?)\s\w+=""",
"""\Wtz="?({tz}[+-]\d+)"""
"""referralurl=({url}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```