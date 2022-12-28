#### Parser Content
```Java
{
Name = pingidentity-pi-cef-endpoint-authentication-fail-failure
Conditions = [
  """CEF:"""
  """|Ping Identity|PingFederate|"""
  """|AUTHN_ATTEMPT|"""
  """msg=failure"""
]
ParserVersion = "v1.0.0"

beyondtrust-pi-app-activity.Fields}[
  """"ElevationGroup\\?"\svalue=\\?"({privileges}[^"\\]+)\\?""""
  """"\ssEventID=\\?"({operation}[^"]+?)\\""""
]
DupFields = [ "account->dest_user", "account_domain->dest_domain","operation->event_name" ]
Conditions = [
  """EVENT_ID_JOB_ACCOUNT_ELEVATION_DEELEVATED"""
  """2053"""
  """sEventID"""
  """dwBasicEventType"""
  """sOriginatingApplicationName"""
  """dwAppSpecificEventID"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
Fields = [
  """\Wrt=({time}\w+\.? \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wduid=({user}[^\s@\\\=]+?)[\\\=]*\s+(\w+=|$)"""
  """\Wduid=({email_address}[^\s@]+@[^\s@]+)"""
  """\Wcs2=(|({connection_id}[^=]+?))\s+(\w+=|$)"""
  """\Wcs3=(|({protocol}[^=]+?))\s+(\w+=|$)"""
  """\Wmsg=(|({result}[^=]+?))\s+(\w+=|$)"""
  """\|Ping Identity\|PingFederate\|([^\|]*){3}\|({event_name}[^\|]+)"""
  """cs6=(|({additional_info}[^"]+?))\s+(\w+=|$)"""
]
Name = pingidentity-pi-cef-endpoint-authentication-fail-failure
Conditions = [
  """CEF:"""
  """|Ping Identity|PingFederate|"""
  """|AUTHN_ATTEMPT|"""
  """msg=failure"""
]
ParserVersion = "v1.0.0"
},

{
Name = "beyondtrust-prividentity-xml-app-activity-success-identity"
Vendor = "BeyondTrust"
Product = "BeyondTrust Privileged Identity"
TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
Conditions = [
"""sEventID="EVENT_ID_JOB_ACCOUNT_ELEVATED""""
"""sOriginatingApplicationName ="Privileged Identity""""
"""<Event """
]
Fields = [
"""\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
"""dtPostTime="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""sEventID="({operation}[^"]+)"""
"""\(running as user (({account_domain}[^\s\\]+)\\+)?({account}[^\s\\\)]+)\)"""
""""AccountToElevate"\s+value="(({domain}[^\s\\]+)\\+)?({user}[^\s\\"]+)"""
"""group '({object}[^\']+)' on system """
""""TargetSystem"\s+value="({dest_host}[^"]+)"""
"""OriginatingApplicationName ="({app}[^"]+)"""
]
ParserVersion = "v1.0.0"
},

${LiebsoftParserTemplates.beyondtrust-pi-app-activity}{
Name = beyondtrust-prividentity-kv-user-privilege-modify-success-jobaccountelevated
Fields = ${LiebsoftParserTemplates.beyondtrust-pi-app-activity.Fields}[
  """"ElevationGroup\\?"\svalue=\\?"({privileges}[^"\\]+)\\?""""
  """"\ssEventID=\\?"({operation}[^"]+?)\\""""
]
DupFields = [ "account->dest_user", "account_domain->dest_domain" ,"operation->event_name"]
Conditions = [
  """EVENT_ID_JOB_ACCOUNT_ELEVATED"""
  """2051"""
  """sEventID"""
  """dwBasicEventType"""
  """sOriginatingApplicationName"""
  """dwAppSpecificEventID"""
  """Privileged Identity"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
Fields = [
  """\Wrt=({time}\w+\.? \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wduid=({user}[^\s@\\\=]+?)[\\\=]*\s+(\w+=|$)"""
  """\Wduid=({email_address}[^\s@]+@[^\s@]+)"""
  """\Wcs2=(|({connection_id}[^=]+?))\s+(\w+=|$)"""
  """\Wcs3=(|({protocol}[^=]+?))\s+(\w+=|$)"""
  """\Wmsg=(|({result}[^=]+?))\s+(\w+=|$)"""
  """\|Ping Identity\|PingFederate\|([^\|]*){3}\|({event_name}[^\|]+)"""
  """cs6=(|({additional_info}[^"]+?))\s+(\w+=|$)"""
]
Name = pingidentity-pi-cef-endpoint-authentication-fail-authfailure
Conditions = [
  """CEF:"""
  """|Ping Identity|PingFederate|"""
  """|OAuth|OAuth|"""
  """msg=failure"""
]
ParserVersion = "v1.0.0"
},

${LiebsoftParserTemplates.beyondtrust-pi-app-activity}{
Name = beyondtrust-prividentity-kv-user-switch-success-passwordcheckedout
Fields = ${LiebsoftParserTemplates.beyondtrust-pi-app-activity.Fields}[
  """sLoginName =\\?"(({domain}[^\\]+)\\+)?({user}[^\\"]+)\\?"""",
  """sMessage=\\?"checked-out password for\s*\([^\)]*\)'(({account_domain}[^\\']+)\\+)?({account}[^\\\s']+)"""
  """"\ssEventID=\\?"({operation}[^"]+?)\\""""
]
DupFields = [ "account->dest_user", "account_domain->dest_domain", "operation->event_name"]
Conditions = [
  """EVENT_ID_PASSWORD_CHECKED_OUT"""
  """2002"""
  """sEventID"""
  """dwBasicEventType"""
  """sOriginatingApplicationName"""
  """dwAppSpecificEventID"""
  """Privileged Identity"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
Fields = [
  """\Wrt=({time}\w+\.? \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wduid=({user}[^\s@\\\=]+?)[\\\=]*\s+(\w+=|$)"""
  """\Wduid=({email_address}[^\s@]+@[^\s@]+)"""
  """\Wcs2=(|({connection_id}[^=]+?))\s+(\w+=|$)"""
  """\Wcs3=(|({protocol}[^=]+?))\s+(\w+=|$)"""
  """\Wmsg=(|({result}[^=]+?))\s+(\w+=|$)"""
  """\|Ping Identity\|PingFederate\|([^\|]*){3}\|({event_name}[^\|]+)"""
  """cs6=(|({additional_info}[^"]+?))\s+(\w+=|$)"""
]
Name = pingidentity-pi-cef-endpoint-authentication-success-authsuccess
Conditions = [
  """CEF"""
  """|Ping Identity|PingFederate|"""
  """|AUTHN_ATTEMPT|"""
  """msg=success"""
]
ParserVersion = "v1.0.0"
},

${LiebsoftParserTemplates.beyondtrust-pi-app-activity}{
Name = beyondtrust-prividentity-kv-user-password-modify-success-sharedcredentiallisteditedaccount
Fields = ${LiebsoftParserTemplates.beyondtrust-pi-app-activity.Fields}[
  """"SharedCredentialAccountName\\?"\svalue=\\?"({dest_user}[^"\\]+)\\?""""
]
Conditions = [
  """EVENT_ID_SHARED_CREDENTIAL_LIST_EDITED_ACCOUNT"""
  """2058"""
  """sEventID"""
  """dwBasicEventType"""
  """sOriginatingApplicationName"""
  """dwAppSpecificEventID"""
  """Privileged Identity"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
Fields = [
  """\Wrt=({time}\w+\.? \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wduid=({user}[^\s@\\\=]+?)[\\\=]*\s+(\w+=|$)"""
  """\Wduid=({email_address}[^\s@]+@[^\s@]+)"""
  """\Wcs2=(|({connection_id}[^=]+?))\s+(\w+=|$)"""
  """\Wcs3=(|({protocol}[^=]+?))\s+(\w+=|$)"""
  """\Wmsg=(|({result}[^=]+?))\s+(\w+=|$)"""
  """\|Ping Identity\|PingFederate\|([^\|]*){3}\|({event_name}[^\|]+)"""
  """cs6=(|({additional_info}[^"]+?))\s+(\w+=|$)"""
]
Name = pingidentity-pi-cef-endpoint-authentication-success-authenticated
Conditions = [
  """CEF"""
  """|Ping Identity|PingFederate|"""
  """|OAuth|OAuth|"""
  """msg=success"""
]
ParserVersion = "v1.0.0"
},

${LiebsoftParserTemplates.beyondtrust-pi-app-activity}{
Name = beyondtrust-prividentity-kv-app-activity-success-webapppasswordcheckin
Conditions = [
  """EVENT_ID_WEBAPP_PASSWORD_CHECKIN"""
  """3018"""
  """sEventID"""
  """dwBasicEventType"""
  """sOriginatingApplicationName"""
  """dwAppSpecificEventID"""
  """Privileged Identity"""
]
ParserVersion = "v1.0.0"
},

{
Name = pingidentity-pingone-sk4-vpn-login-success-sso
Vendor = Ping Identity
Product = PingOne
TimeFormat = "epoch"
Conditions = [
  """destinationServiceName =Ping"""
  """flexString2=SSO"""
  """request=Success"""
]
Fields = [
  """end=({time}\d{13})"""
  """cat=({category}[^\s]+)"""
  """request=({result}[^\s]+)"""
  """requestClientApplication=({app}.*?)\s\w+="""
  """suser=({user}[^\s]+)"""
  """flexString2=({auth_method}.*?)\s\w+"""
  """message":"({auth_method}[^\\]+)\s\"({device_name}[^\\]+)"""
]
ParserVersion = "v1.0.0"
},

${LiebsoftParserTemplates.beyondtrust-pi-app-activity}{
Name = beyondtrust-prividentity-kv-app-activity-success-passwordcheckedin
Conditions = [
  """EVENT_ID_PASSWORD_CHECKED_IN"""
  """2003"""
  """sEventID"""
  """dwBasicEventType"""
  """sOriginatingApplicationName"""
  """dwAppSpecificEventID"""
  """Privileged Identity"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
Fields = [
  """\Wrt=({time}\w+\.? \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wduid=({user}[^\s@\\\=]+?)[\\\=]*\s+(\w+=|$)"""
  """\Wduid=({email_address}[^\s@]+@[^\s@]+)"""
  """\Wcs2=(|({connection_id}[^=]+?))\s+(\w+=|$)"""
  """\Wcs3=(|({protocol}[^=]+?))\s+(\w+=|$)"""
  """\Wmsg=(|({result}[^=]+?))\s+(\w+=|$)"""
  """\|Ping Identity\|PingFederate\|([^\|]*){3}\|({event_name}[^\|]+)"""
  """cs6=(|({additional_info}[^"]+?))\s+(\w+=|$)"""
]
Name = pingidentity-pi-cef-endpoint-authentication-fail-authnattemptfail
Conditions = [
  """CEF:"""
  """|Ping Identity|PingFederate|"""
  """|AUTHN_ATTEMPT|"""
  """msg=failure"""
]
ParserVersion = "v1.0.0"
},

${LiebsoftParserTemplates.beyondtrust-pi-app-activity}{
Name = beyondtrust-prividentity-kv-app-activity-success-passwordchangeonsystem
Conditions = [
  """EVENT_ID_JOB_STARTING_PASSWORD_CHANGE_ON_SYSTEM"""
  """2013"""
  """sEventID"""
  """dwBasicEventType"""
  """sOriginatingApplicationName"""
  """dwAppSpecificEventID"""
  """Privileged Identity"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
Fields = [
  """\Wrt=({time}\w+\.? \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wduid=({user}[^\s@\\\=]+?)[\\\=]*\s+(\w+=|$)"""
  """\Wduid=({email_address}[^\s@]+@[^\s@]+)"""
  """\Wcs2=(|({connection_id}[^=]+?))\s+(\w+=|$)"""
  """\Wcs3=(|({protocol}[^=]+?))\s+(\w+=|$)"""
  """\Wmsg=(|({result}[^=]+?))\s+(\w+=|$)"""
  """\|Ping Identity\|PingFederate\|([^\|]*){3}\|({event_name}[^\|]+)"""
  """cs6=(|({additional_info}[^"]+?))\s+(\w+=|$)"""
]
Name = pingidentity-pi-cef-endpoint-authentication-fail-failure-1
Conditions = [
  """CEF:"""
  """|Ping Identity|PingFederate|"""
  """|OAuth|OAuth|"""
  """msg=failure"""
]
ParserVersion = "v1.0.0"
},

${LiebsoftParserTemplates.beyondtrust-pi-app-activity}{
Name = beyondtrust-prividentity-kv-app-activity-success-passwordcheckoutexpired
Conditions = [
  """EVENT_ID_PASSWORD_CHECKOUT_EXPIRED"""
  """2004"""
  """sEventID"""
  """dwBasicEventType"""
  """sOriginatingApplicationName"""
  """dwAppSpecificEventID"""
  """Privileged Identity"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*(uid=({user}[^,]+)[^|]+?|AWSCentrifyAPI-Puppet|({=user}[^\s\|@]+))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*({email_address}[^\s\|@]+@({email_domain}[^\s\|@]+))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){1}\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){4}\s*({protocol}[^\s\|]+)"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){7}\s*({result}[^\s\|]+)"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){2}\s*(|({app}[^\|]*?))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){5}\s*(|({host_ip}[A-Fa-f\d:.]*?)|({host}[\w\-.]+))\s*\|"""
]
DupFields = [
  "protocol->auth_method"
]
Name = pingidentity-pi-str-endpoint-authentication-success-authnattemptsuccess
Conditions = [
  """|AUTHN_ATTEMPT|"""
  """success|"""
]
ParserVersion = "v1.0.0"
},

${LiebsoftParserTemplates.beyondtrust-pi-app-activity}{
Name = beyondtrust-prividentity-kv-app-activity-success-sharedcredentiallistremovedaccount
Conditions = [
  """EVENT_ID_SHARED_CREDENTIAL_LIST_REMOVED_ACCOUNT"""
  """2059"""
  """sEventID"""
  """dwBasicEventType"""
  """sOriginatingApplicationName"""
  """dwAppSpecificEventID"""
  """Privileged Identity"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*(uid=({user}[^,]+)[^|]+?|AWSCentrifyAPI-Puppet|({=user}[^\s\|@]+))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*({email_address}[^\s\|@]+@({email_domain}[^\s\|@]+))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){1}\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){4}\s*({protocol}[^\s\|]+)"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){7}\s*({result}[^\s\|]+)"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){2}\s*(|({app}[^\|]*?))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){5}\s*(|({host_ip}[A-Fa-f\d:.]*?)|({host}[\w\-.]+))\s*\|"""
]
DupFields = [
  "protocol->auth_method"
]
Name = pingidentity-pi-str-endpoint-authentication-success-oauthsuccess
Conditions = [
  """|OAuth|"""
  """success|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*(uid=({user}[^,]+)[^|]+?|AWSCentrifyAPI-Puppet|({=user}[^\s\|@]+))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*({email_address}[^\s\|@]+@({email_domain}[^\s\|@]+))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){1}\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){4}\s*({protocol}[^\s\|]+)"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){7}\s*({result}[^\s\|]+)"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){2}\s*(|({app}[^\|]*?))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){5}\s*(|({host_ip}[A-Fa-f\d:.]*?)|({host}[\w\-.]+))\s*\|"""
]
DupFields = [
  "protocol->auth_method"
]
Name = pingidentity-pi-str-endpoint-authentication-success-authnsessioncreated
Conditions = [
  """| AUTHN_SESSION_CREATED|"""
  """success|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*(uid=({user}[^,]+)[^|]+?|AWSCentrifyAPI-Puppet|({=user}[^\s\|@]+))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*({email_address}[^\s\|@]+@({email_domain}[^\s\|@]+))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){1}\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){4}\s*({protocol}[^\s\|]+)"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){7}\s*({result}[^\s\|]+)"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){2}\s*(|({app}[^\|]*?))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){5}\s*(|({host_ip}[A-Fa-f\d:.]*?)|({host}[\w\-.]+))\s*\|"""
]
DupFields = [
  "protocol->auth_method"
]
Name = pingidentity-pi-str-endpoint-authentication-success-authsessionused
Conditions = [
  """| AUTHN_SESSION_USED|"""
  """success|"""
]
ParserVersion = "v1.0.0"
},

{
Name = pingidentity-pi-json-endpoint-authentication-success-fail-idp
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """SSO_CALL":"""
  """Sensitive":"""
  """Status":"""
  """Transaction_ID":"""
]
Fields = [
  """"@timestamp"+:"+({time}[^"]+)"""
  """"+hostname"+:"+({host}[^"]+)"""
  """"+SAML_Subject"+:"+({email_address}[^"]+)"""
  """"+Sensitive"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"+SSO_CALL"+:"+({auth_method}[^"]+)"""
  """"+Application"+:"+\s(\s|({service_name}[^"]+))"""
  """"+Status"+:"+({result}[^"]+)"""
  """"+Sensitive_IAM_Server"+:"+({auth_server}[^"]+)"""
  """"+Protocol"+:"+({protocol}[^"]+)"""
  """"+Event"+:"+({operation}[^"]+)"""
  """"+ERROR"+:"+({failure_reason}[^"]+)"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*(uid=({user}[^,]+)[^|]+?|AWSCentrifyAPI-Puppet|({=user}[^\s\|@]+))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*({email_address}[^\s\|@]+@({email_domain}[^\s\|@]+))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){1}\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){4}\s*({protocol}[^\s\|]+)"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){7}\s*({result}[^\s\|]+)"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){2}\s*(|({app}[^\|]*?))\s*\|"""
  """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){5}\s*(|({host_ip}[A-Fa-f\d:.]*?)|({host}[\w\-.]+))\s*\|"""
]
DupFields = [
  "protocol->auth_method"
]
Name = pingidentity-pi-str-endpoint-login-success-stssuccess
Conditions = [
  """| STS|"""
  """success|"""
]
ParserVersion = "v1.0.0"
},

${LiebsoftParserTemplates.beyondtrust-pi-app-activity}{
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
  Name = avaya-ers-str-endpoint-login-fail-intruderip
  Vendor = Avaya
  Product = Avaya Ethernet Routing Switch
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """:Authentication Failure""", """Server IP""", """Intruder IP""" ]
  Fields = [
    """({event_name}Authentication Failure)""",
    """Server IP\s+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Intruder IP\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = axway-gateway-str-endpoint-login-success-successfullogin
  Vendor = Axway
  Product = Axway Gateway
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """user:INFO""", """SSH: Successful login on""", """Username:""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({event_name}Successful login)""",
    """Successful login on\s*\[?({dest_ip}[a-fA-F\d.:]+)\]?""",
    """Username:\s*"+({user}[^"]+)""",
    """({auth_package}SSH)"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = barracuda-firewall-str-endpoint-login-fail-denied
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ LOGIN ATTEMPT: """, """ Security """, """: Denied: """, """: Login """, """box_Auth_access:""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)""",
    """Login (|({user}[^\s]+)\s)from ({src_ip}[a-fA-F\d:.]+)\s*:\s*({action}[^:.]+)(:|\.)""",
    """({event_name}LOGIN ATTEMPT)"""
  """Denied:\s({failure_reason}[^$]+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = barracuda-firewall-str-endpoint-login-allowed
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ LOGIN ATTEMPT: """, """ Info """, """ : Allowed""", """box_Auth_access:""", """: Login """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)""",
    """Login (|({user}[^\s]+)\s)from ({src_ip}[a-fA-F\d:.]+)\s*:\s*({action}[^:.]+)(:|\.)""",
    """({event_name}LOGIN ATTEMPT)"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = vmware-carbonblack-sk4-endpoint-login-success-cbdefense
  Vendor = VMware
  Product = Carbon Black CES
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =CB Defense""", """"loginName":""", """Logged in successfully""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"loginName":"(({user}[^"@]+)|({email_address}[^"]+@[^"]+))"""",
    """clientIp":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """description":"({event_name}[^"]+)""",
    """({app}CB Defense)"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = opendj-o-kv-endpoint-login-msgid
  Vendor = OpenDJ
  Product = OpenDJ
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """] BIND RES conn=""", """etime=""", """op=""", """msgID=""", """result=""" ]
  Fields = [
    """\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [-\+]\d+)\]""",
    """conn=({connection_id}\d+)""",
    """authFailureReason="({failure_reason}[^"]+)""",
    """authDN="({auth_dn}[^"]+)"""
    """uid=({user_uid}\d+)"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = opendj-o-kv-endpoint-login-connectconn
  Vendor = OpenDJ
  Product = OpenDJ
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """from=""", """to=""", """] CONNECT conn=""", """protocol=LDAP""" ]
  Fields = [
    """\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [-\+]\d+)\]""",
    """conn=({connection_id}\d+)""",
    """from=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """to=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))""",
    """protocol=({auth_method}[^\s]+)"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = opendj-o-kv-endpoint-login-uid
  Vendor = OpenDJ
  Product = OpenDJ
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """uid=""", """ REQ conn=""", """op=""", """msgID=""" ]
  Fields = [
    """\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [-\+]\d+)\]""",
    """conn=({connection_id}\d+)""",
    """uid=({user_uid}\d+)"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = dtexsystems-intercept-cef-endpoint-login-success-sessionlogon
  Vendor = Dtex Systems
  Product = DTEX InTERCEPT
  TimeFormat = "epoch"
  Conditions = [ "CEF:", """|Dtex|""", """|SessionActivity|SessionLogon|""" ]
  Fields = [
    """\Wstart=({time}\d{13})""",
    """\WDevice_Name =(({domain}[^\\]+)\\+)?({host}[^\\\s]+)""",
    """\WUser_Name =(({domain}[^\\]+)\\+)?({user}[^\\\s]+)\s""",
    """\|Dtex\|([^\|]*\|){2}(SessionActivity\|)?({event_code}[^\|]+)\|""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"
},

{
  Name = dell-emcisilon-str-file-read-success-open
  ParserVersion = v1.0.0
  Vendor = Dell
  Product = EMC Isilon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """|SMB|""","""|OPEN|""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+(([\+\-]\d+:\d+)|Z))\s+({host}[\w\-.]+)\s+([^\[\s]*)?\[[^\]]*\]:?\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({server_name}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}[A-Fa-f:\d.]+)\|({protocol}[^\|]*)\|({access}OPEN)\|({result}[^\|\s]*)\|({desire_access}[^\|]*)\|({file_type}[^\|]*)\|({create_result}[^\|]*)\|(|({inode}[^\|]*))\|({file_path}({file_dir}[^"]+[\\\/])?({file_name}[^"]+(\.({file_ext}[^"]+)?)\s+)?)""",
  
}
```