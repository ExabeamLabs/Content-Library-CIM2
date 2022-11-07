#### Parser Content
```Java
{
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

beyondtrust-pi-app-activity = {
    Vendor = BeyondTrust
    Product = BeyondTrust Privileged Identity
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
    Fields = [
      """dtPostTime=\\?"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
      """hostname":"({host}[^"]+)""""
      """\ssIpAddress=\\?"({src_ip}[a-fA-F\d:.]+)"""
      """\ssEventID=\\?"({operation}[^"]+?)\\?""""
      """\ssOriginatingApplicationName =\\?"({app}[^"\\]+?)\\?""""
      """dwAppSpecificEventID=\\?"({event_code}\d+)"""
      """\ssOriginatingAccount=\\?"(({domain}[^\\]+)\\+)?({user}[^"\\]+?)\\?""""
      """\ssOriginatingSystem=\\?"({src_host}[^"\\]+?)\\?""""
      """"sAccountName\\?"\svalue=\\?"({account}[^"\\]+)\\?""""
      """key=\\?"AccountToElevate\\?"\svalue=\\?"(({account_domain}[^\\]+)\\+)?({account}[^"\\]+?)\\?""""
      """\ssMessage=\\?"({additional_info}[^\n>]+?)(>|\\r","exa_rsc":)"""
      """"(sSystemName|TargetSystem)\\?"\svalue=\\?"({dest_host}[\w\-.]+)\\?""""
    ]
    DupFields = [ "operation->event_name" ]
 }

}

HornetDlpEmailTemplates = {
  hornet-dlp-email = {
    Vendor = Hornet
    Product = Hornet Email
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Fields = [
      """date=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """dir=({direction}1|2)""",
      """main_domain=({domain}[^=]+?)\s*(\w+=|$)""",
      """from=({email_address}[^@\s]+?@[^\s]+)""",
      """to=({dest_email_address}[^@\s]+?@[^\s]+)""",
      """\stype=({result}\d+)""",
      """reason="({additional_info}[^"]+)""",
      """src_host=((?i)unknown|({src_host}[^\s]+))""",
      """src_ip=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """dst_ip=(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+))""",
      """msgid="({message_id}[^"]+)""",
      """subject="[\s ]*({email_subject}[^"]+?)[\s ]*"""",
      """attachments="[^0"]#({email_attachments}[^"]+)""",
    
}
```