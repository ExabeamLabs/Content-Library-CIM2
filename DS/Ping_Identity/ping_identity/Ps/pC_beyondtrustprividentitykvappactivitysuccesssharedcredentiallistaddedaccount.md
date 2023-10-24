#### Parser Content
```Java
{
Name = beyondtrust-prividentity-kv-app-activity-success-sharedcredentiallistaddedaccount
Conditions = [
  """EVENT_ID_SHARED_CREDENTIAL_LIST_ADDED_ACCOUNT"""
  """2057"""
  """sEventID"""
  """dwBasicEventType"""
  """sOriginatingApplicationName"""
  """dwAppSpecificEventID"""
  """Privileged Identity"""
]
ParserVersion = "v1.0.0"

beyondtrust-pi-app-activity}{
Name = beyondtrust-prividentity-kv-app-activity-success-sharedcredentiallistaddedaccount
Conditions = [
  """EVENT_ID_SHARED_CREDENTIAL_LIST_ADDED_ACCOUNT"""
  """2057"""
  """sEventID"""
  """dwBasicEventType"""
  """sOriginatingApplicationName"""
  """dwAppSpecificEventID"""
  """Privileged Identity"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Ping Identity"
Product = "Ping Identity"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*(uid=({user}[\w\.\-]{1,40}\$?)[^|]+?|AWSCentrifyAPI-Puppet|({=user}[^\s\|@]+))\s*\|"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*({email_address}[^\s\|@]+@({email_domain}[^\s\|@]+))\s*\|"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){1}\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){4}\s*({protocol}[^\s\|]+)"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){7}\s*({result}[^\s\|]+)"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){2}\s*(|({app}[^\|]*?))\s*\|"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){5}\s*(|({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({host}[\w\-.]+))\s*\|"""
]
DupFields = [
"protocol->auth_method"
]
Name = "pingidentity-pi-cef-app-login-success-pingfederate"
Conditions = [
"""|SSO|"""
"""success|"""
]
ParserVersion = "v1.0.0"
},

${PingParsersTemplates.cef-ping-events-1}{
  Name = pingidentity-pi-cef-app-login-success-sso
  Conditions = [ """CEF""", """|Ping Identity|PingFederate|""", """|SSO|""", """msg=success""" ]
  ParserVersion = "v1.0.0"
},

{
  Name = pingidentity-pingone-sk4-app-login-success-loginsuccess
  Vendor = Ping Identity
  Product = PingOne
  TimeFormat = "epoch"
  Conditions = [ """destinationServiceName =Ping""", """|login-success|""" ]
  Fields = [
    """end=({time}\d{13})""",
    """cat=({category}[^\s]+)"""
    """request=({result}[^\s]+)""",
    """requestClientApplication=({app}.*?)\s\w+=""",
    """suser=({user}[\w\.\-]{1,40}\$?)""",
    """flexString2=({auth_method}.*?)\s\w+="""
  ]
  ParserVersion = "v1.0.0"
},

${PingParsersTemplates.cef-ping-events-1}{
  Name = pingidentity-pi-cef-endpoint-authentication-success-authnsessioncreated
  Conditions = [ """CEF""", """|Ping Identity|PingFederate|""", """|AUTHN_SESSION_CREATED|AUTHN_SESSION_CREATED|""", """msg=success""" ]
  ParserVersion = "v1.0.0"
},

${PingParsersTemplates.cef-ping-events-1}{
  Name = pingidentity-pi-cef-app-login-fail-sso
  Conditions = [ """CEF:""", """|Ping Identity|PingFederate|""", """|SSO|""", """msg=failure""" ]
  ParserVersion = "v1.0.0"
},

{
  Name = pingidentity-pi-kv-app-login-success-sso
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """event=SSO""", """status=success""",""" pfhost=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),""",
    """\sip=(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s\w+=""",
    """\spfhost=(|({host}[^=\s]+?))\s\w+=""",
    """\ssubject="(|(({email_address}[^"@\s]+@[^"@\s]+)|({user}[\w\.\-]{1,40}\$?)))"""",
    """\sapp=(|({app}[^=]+?))\s\w+="""
  ]
  ParserVersion = "v1.0.0"
},
${PingParsersTemplates.ping-events-3}{
  Name = pingidentity-pi-kv-app-authentication-failure
  ParserVersion = "v1.0.0"
  Conditions = [
     """event=AUTHN_ATTEMPT"""
     """status=failure"""
     """pfhost="""
   
}
```