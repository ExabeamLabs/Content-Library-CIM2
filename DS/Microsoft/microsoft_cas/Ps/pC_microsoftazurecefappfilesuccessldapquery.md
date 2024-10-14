#### Parser Content
```Java
{
Name = microsoft-azure-cef-app-file-success-ldapquery
  Product = Microsoft CAS
  ParserVersion = v1.0.0
  Conditions = [ """"eventTypeName":"""", """"genericEventType":"""", """"aadTenantId":"""", """LDAP query""", """Run command:""", """"type":"run"""" ]
  Fields = ${MSParsersTemplates.cef-azure-app-activity-1.Fields}[
    """\suser\s<b>(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^<]+))<\/b>"""
    """\sgroup\s<b>({group_name}[^<]+)<\/b>"""
    """SourceComputerObjectGuid[^\s]+\s+<b>({process_guid}[^<]+)<\/b>"""
    """SourceComputerDnsName[^\s]+\s+<b>({src_host}[^<]+)<\/b>"""
    """SourceComputerOperatingSystem<[^\s]+\s+<b>({os}[^<]+)<\/b>"""
    """DestinationComputerDnsName[^\s]+\s+<b>({dest_host}[^<]+)<\/b>"""
    """SourceAccountId[^\s]+\s+<b>({account_id}[^<]+)<\/b>"""
    """SourceAccountSid[^\s]+\s+<b>({user_sid}[^<]+)<\/b>"""
    """TargetAccountSid[^\s]+\s+<b>({dest_user_sid}[^<]+)<\/b>"""
    """TargetAccountUpnName[^\s]+\s+<b>({user_upn}[^<]+)<\/b>"""
    """Category[^\s]+\s+<b>({category}[^<]+)<\/b>"""
    """AttackTechniques[^\s]+\s+<b>({attack_info}[^<]+)<\/b>"""
    """Protocol[^\s]+\s+<b>({protocol}[^<]+)<\/b>"""    
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

}
```