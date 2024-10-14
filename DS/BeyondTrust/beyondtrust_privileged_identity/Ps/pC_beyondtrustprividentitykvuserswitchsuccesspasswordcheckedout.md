#### Parser Content
```Java
{
Name = beyondtrust-prividentity-kv-user-switch-success-passwordcheckedout
Fields = ${BeyondTrustParserTemplates.beyondtrust-pi-app-activity.Fields}[
  """sLoginName =\\?"(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?"""",
  """sMessage=\\?"checked-out password for\s*\([^\)]*\)'(({account_domain}[^\\']+)\\+)?({account}[^\\\s']+)"""
  """"\ssEventID=\\?"({operation}[^"]+?)\\""""
]
DupFields = ${BeyondTrustParserTemplates.beyondtrust-pi-app-activity.DupFields}[ "account->dest_user", "account_domain->dest_domain", "operation->event_name"]
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

beyondtrust-pi-app-activity = {
    Vendor = BeyondTrust
    Product = BeyondTrust Privileged Identity
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
    Fields = [
      """dtPostTime=\\?"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
      """hostname":"({host}[^"]+)""""
      """\ssIpAddress=\\?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """\ssEventID=\\?"({operation}[^"]+?)\\?""""
      """\ssOriginatingApplicationName =\\?"({app}[^"\\]+?)\\?""""
      """dwAppSpecificEventID=\\?"({event_code}\d+)"""
      """\ssOriginatingAccount=\\?"(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?""""
      """\ssOriginatingSystem=\\?"({src_host}[^"\\]+?)\\?""""
      """"sAccountName\\?"\svalue=\\?"({account}[^"\\]+)\\?""""
      """key=\\?"AccountToElevate\\?"\svalue=\\?"(({account_domain}[^\\]+)\\+)?({account}[^"\\]+?)\\?""""
      """\ssMessage=\\?"({additional_info}[^\n]+?)(\\r","exa_rsc":)"""
      """"(sSystemName|TargetSystem)\\?"\svalue=\\?"({dest_host}[\w\-.]+)\\?""""
    ]
    DupFields = [ "operation->event_name" ]
 }

   lieberman-events = {
      Vendor = BeyondTrust
      Product = BeyondTrust Privileged Identity
      TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
      Fields = [
        """({host}\S+)\s+<Event"""
        """dwAppSpecificEventID="({event_code}\d+)"""
        """sEventID="({event_name}[^"]+)"""
        """sOriginatingApplicationName ="({app}[^"]+)"""
        """sOriginatingSystem="({src_host}[^"]+)"""
        """sOriginatingAccount="(({account_domain}[^\\]+)[\\]+)?({account}[^\s"]+)""""
        """dtPostTime="({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
        """sMessage="({additional_info}[^"]+)"""
        """sLoginName ="(({domain}[^\\]+)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
# job_id is removed
        """sIpAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
        
}
```