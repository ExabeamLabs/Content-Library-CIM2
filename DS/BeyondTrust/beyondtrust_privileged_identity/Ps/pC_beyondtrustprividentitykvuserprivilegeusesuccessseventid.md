#### Parser Content
```Java
{
Name = "beyondtrust-prividentity-kv-user-privilege-use-success-seventid"
Vendor = "BeyondTrust"
Product = "BeyondTrust Privileged Identity"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """Enterprise Random Password Manager"""
  """sEventID"""
  """dwBasicEventType"""
]
Fields = [
  """"@timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)Z\""""
  """\d\d:\d\d:\d\d\s({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """"hostname\":\"({host}[^\"]+)\""""
  """sEventID=\\\"({event_name}[^\"]+)\\\""""
  """sOriginatingSystem=\\\"({src_host}[^\"]+)\\\""""
  """"(sSystemName|TargetSystem)\\\"\svalue=\\\"({dest_host}[^\"]+)\\\""""
  """"AccountTargetName\\\"\svalue=\\\"({account}[^\"]+)\\\""""
  """sOriginatingAccount=\\\"(({domain}[^\\\"]+?)\\+)?({user}[\w\.\-]{1,40}\$?)\\\""""
  """sLoginName =\\\"(({dest_domain}[^\\\"]+)\\+)?({dest_user}[^\"]+)\\\""""
  """"AccountToElevate\\\"\svalue=\\\"(({dest_domain}[^\\\"]+)\\+)?({dest_user}[^\"]+)\\\""""
  """ElevationGroup\\\"\svalue=\\\"({privileges}[^\"]+)\\\""""
  """sEventType=\\\"({event_category}[^\"]+)\\\""""
]
DupFields = [
  "account->object"
]
ParserVersion = "v1.0.0"


}
```