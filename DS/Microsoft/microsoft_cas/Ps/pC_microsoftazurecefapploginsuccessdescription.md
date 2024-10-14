#### Parser Content
```Java
{
Name = "microsoft-azure-cef-app-login-success-description"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Microsoft CAS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""eventTypeName":""""
""""genericEventType":""""
""""aadTenantId":""""
"""description":"Log on""""
""""type":"login""""
]
Fields = [
"""\Wdvc=(Unknown|Personal|({host}\S+))"""
"""\Wdvchost=(?:Unknown|Personal|({host}[\w\-.]+))\s+\w+="""
"""act=({operation}[^\s]+)\s+(\w+=|$)"""
"""\Wrt=({time}\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) \S+ """
"""\Wduser=(anonymous|Unknown|email|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""\Wsuser=(anonymous|Unknown|email|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""\Woutcome=({result}[^\s]+)\s+(\w+=|$)"""
"""CEF:([^\|]*\|){2}({app}[^\|]+)"""
"""destinationServiceName =({app}[^=]+?)\s+(\w+=|$)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"description\":\"({additional_info}[^\"]+?)\s*\""""
"""\"SourceAccountDisplayName\",\"value\":\"({full_name}({first_name}[^\s\"]+)\s({last_name}[^\s\"]+))\""""
"""\"SourceAccountUpnName\",\"value\":\"({email_address}[^@\"]+@({email_domain}[^\"]+))\""""
"""\"SourceComputerDnsName\",\"value\":\"({src_host}[^\"]+)\""""
"""\"DestinationComputerDnsName\",\"value\":\"({dest_host}[\w\-.]+)\""""
"""\"DestinationIpAddress\",\"value\":\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
"""\"Protocol\",\"value\":\"({protocol}[^\"]+)\""""
"""\"1\":[^=]+?\"displayName\":\"\s*(_splunk_exo|({full_name}({last_name}[^, \"]+)[,\s]+({first_name}[^\"\(]+?))\s*|({email_address}[^@\"]+@({email_domain}[^@\"]+?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\([^\"]+\))?\""""
"""device <b>({dest_host}[\w\-.]+)"""
"""\"userAgent\":\";*({user_agent}[^\"]+?);*\""""
"""\"countryCode\":\"(--|({country_code}[^\"]+))\""""
"""\"Upn\":\"(anonymous|email|({email_address}[^@\"]+@({email_domain}[^@\"]+?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\""""
"""\"appName\":\"({app}[^\",]+)\"""",
""""browser":"({browser}[^"]+)"""",
""""os":"({os}[^"]+)"""",
""""type":"({operation}[^"]+)"""",
""""prettyOperationName":"({operation}[^"]+)"""",
""""rawOperationName":"({operation}[^"]+)"""",
"""app-user-id":"({user_id}[\w-]+)""",
"""src-ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""activityResult":[^}]+?"isSuccess":({result}(?i)(true|false))""",
""""eventTypeName":"({event_name}[^"]+)""""
"""LoginErrorCode"*:({error_code}\d+)"""
]


}
```