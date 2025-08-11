#### Parser Content
```Java
{
Name = microsoft-o365-cef-email-send-sendas
  ParserVersion = v1.0.0
  Conditions = [
    """Workload""",
    """ClientProcessName""",
    """Subject""",
    """"SendAs"""
  ]
 
o365-dlp-email-out = {
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"CreationTime\\*"+:[\s\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"host\\*"+:[\s\\]*"+({host}[^"\\]+)""",
    """"ResultStatus\\*"+:[\s\\]*"+({result}[^"\\]+)""",
    """"ClientIPAddress\\*"+:[\s\\]*"+\[?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_id}[^"]+)))"+""",
    """"MailboxOwnerUPN\\*"+:[\s\\]*"+({email_address}[^"\\]+)""",
    """"SendAsUserSmtp\\*"+:[\s\\]*"+({additional_info}[^"\\]+)""",
    """"SendOnBehalfOfUserSmtp\\*"+:[\s\\]*"+({additional_info}[^"\\]+)""",
    """"Attachments\\*"+:[\s\\]*"+\s*({email_attachments}[^\n]+?)\s*\\?","\w+":""",
    """"Attachments\\*"+:[\s\\]*"+\s*(-|none|({email_attachments}({email_attachment}[^",;:]+)[^"\\:]*))\s*""",
    """"Subject\\*"+:[\s\\]*"+\s*({email_subject}[^"]+?)\s*\\?"""",
    """"ClientInfoString\\*"+:[\s\\]*"+Client\\*=({alert_name}[^"\\;]+)""",
    """"ActorInfoString\\*"+:[\s\\]*"({user_agent}[^"\\]+)"""
    """src-account-name":"({account_name}[^"]+)""",
    """"SizeInBytes":({bytes}\d+)""",
    """"Workload":\s*"({app}[^"]+)""""
    """"UserType":"*({user_type}[^,}"]+)"*"""
  ]
  DupFields = [ "alert_name->alert_type" ]
 },

cef-azure-app-activity-2 = {
Vendor = Microsoft
Product = Azure
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
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
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"description\":\"({additional_info}[^\"]+?)\s*\""""
"""\"SourceAccountDisplayName\",\"value\":\"({full_name}({first_name}[^\s\"]+)\s({last_name}[^\s\"]+))\""""
"""\"SourceAccountUpnName\",\"value\":\"({email_address}[^@\"]+@({email_domain}[^\"]+))\""""
"""\"SourceComputerDnsName\",\"value\":\"({src_host}[^\"]+)\""""
"""\"DestinationComputerDnsName\",\"value\":\"({dest_host}[\w\-.]+)\""""
"""\"DestinationIpAddress\",\"value\":\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
"""\"Protocol\",\"value\":\"({protocol}[^\"]+)\""""

}
```