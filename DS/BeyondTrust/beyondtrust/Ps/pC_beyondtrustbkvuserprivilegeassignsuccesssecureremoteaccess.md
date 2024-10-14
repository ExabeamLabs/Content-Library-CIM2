#### Parser Content
```Java
{
Name = "beyondtrust-b-kv-user-privilege-assign-success-secureremoteaccess"
Vendor = "BeyondTrust"
Product = "BeyondTrust"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """|BeyondTrust|Secure Remote Access|"""
  """|deviceHost="""
  """|sessionId="""
  """|externalKeyLabel="""
]
Fields = [
  """sessionId=({session_id}[^\|]+)"""
  """deviceHost=({host}[^\|]+)"""
  """dstUser=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """srcUser=({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)\|"""
  """srcUser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\|\w+="""
  """sessionOwner=({full_name}[^\|]+)"""
  """\|BeyondTrust\|Secure Remote Access\|(?:[^\|]+\|){2}({event_name}[^\|]+)\|"""
  """srcHost=({src_host}[^\|]+)"""
  """srcAddr=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|"""
  """srcPort=({src_port}\d+)"""
  """dstHost=({dest_host}[^\|]+)"""
  """dstAddr=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\|"""
  """dstPort=({dest_port}\d+)"""
  """confMemOs=({os}[^\|]+)"""
  """cmdShellViewUrl=({additional_info}[^\|]+)"""
]
DupFields = [
  "dest_user->account"
]
ParserVersion = "v1.0.0"


}
```