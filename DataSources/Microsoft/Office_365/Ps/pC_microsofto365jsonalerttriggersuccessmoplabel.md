#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-moplabel
Vendor = "Microsoft"
Product = "Office 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """Workload"""
  """"RuleName""""
  """"PolicyDetails""""
  """Operation"""
]
Fields = [
  """"*CreationTime"*:\s*"*({time}\d+-\d+-\d+T\d+:\d+:\d+)"*"""
  """Workload"*:\s*"*({app}[^"]+)""""
  """ObjectId"*:\s*"*<?({object}[^"]+?)>?""""
  """Operation"*:\s*"*({operation}[^"]+)"*"""
  """UserId"*:\s*"*({email_address}[^@]+@({email_domain}[^"]+))"*"""
  """FileSize"*:\s*"*({bytes}\d+)"""
  """From"*:\s*"*({sender}[^"]+)""""
  """To"*:\s*\["*({recipient}[^"]+)"""
  """Subject"*:\s*"*({alert_subject}[^"]+?)\s*""""
  """MessageID"*:\s*"*<?({message_id}[^"]+?)>?""""
  """Severity"*:\s*"*({alert_severity}[^"]+)""""
  """IncidentId"*:\s*"*({alert_id}[^"]+)""""
  """Actions"*:\s*\["*({action}[^"\]]+?)\s*""""
  """RuleName"*:\s*"*(|({alert_name}.+?[^"]))""""
  """FileName"*:\s*"*(|({file_name}.+?[^"]))""""
  """RecipientCount"*:\s*({recipient_count}\d+)"""
]
DupFields = [
  "sender->email_address"
  "recipient->recipients"
  "operation->alert_type"
]
ParserVersion = "v1.0.0"


}
```