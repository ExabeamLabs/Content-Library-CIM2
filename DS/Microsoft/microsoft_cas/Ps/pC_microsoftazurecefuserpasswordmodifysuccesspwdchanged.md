#### Parser Content
```Java
{
Name = microsoft-azure-cef-user-password-modify-success-pwdchanged
  Product = Microsoft CAS
  ParserVersion = v1.0.0
  Conditions = [
"""CEF:"""
"""destinationServiceName =Office 365"""
"""description":"Change password:"""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-app-activity-1.Fields}[
"""\"description\":\"[^\"]*?device <b>({src_host}[^\"<]+)"""
 ]

cef-azure-app-activity-1 = {
Vendor = Microsoft
Product = Azure
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
"""\Wdvc=(Unknown|Personal|({host}\S+))"""
"""\Wdvchost=(?:Unknown|Personal|({host}[\w\-.]+))\s+\w+="""
"""act=({operation}[^\s]+)\s+(\w+=|$)"""
"""\Wrt=({time}\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) \S+ """
"""\Wduser=(anonymous|Unknown|email|({email_address}[^@=]+@({email_domain}[^@=]+?))|({user}[^=]+?))(\s+\w+=|\s*$)"""
"""\Wsuser=(anonymous|Unknown|email|({email_address}[^@=]+@({email_domain}[^@=]+?))|({user}[^=]+?))(\s+\w+=|\s*$)"""
"""\Woutcome=({result}[^\s]+)\s+(\w+=|$)"""
"""CEF:([^\|]*\|){2}({app}[^\|]+)"""
"""destinationServiceName =({app}[^=]+?)\s+(\w+=|$)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"description\":\"({additional_info}[^\"]+?)\s*\""""
"""\"SourceAccountDisplayName\",\"value\":\"({full_name}({first_name}[^\s\"]+)\s({last_name}[^\s\"]+))\""""
"""\"SourceAccountUpnName\",\"value\":\"({email_address}[^@\"]+@({email_domain}[^\"]+))\""""
"""\"SourceComputerDnsName\",\"value\":\"({src_host}[^\"]+)\""""
"""\"DestinationComputerDnsName\",\"value\":\"({dest_host}[^\"]+)\""""
"""\"DestinationIpAddress\",\"value\":\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
"""\"Protocol\",\"value\":\"({protocol}[^\"]+)\""""

}
```