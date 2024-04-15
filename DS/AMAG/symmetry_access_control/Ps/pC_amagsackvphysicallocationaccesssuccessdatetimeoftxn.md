#### Parser Content
```Java
{
Name = "amag-sac-kv-physical-location-access-success-datetimeoftxn"
Vendor = "AMAG"
Product = "Symmetry Access Control"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """WhereName =""""
  """TxnConditionName =""""
  """DateTimeOfTxn=""""
]
Fields = [
  """[^\w]DateTimeOfTxn="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """[^\w]TxnConditionName ="(\s+|({result}[^"]+))""""
  """[^\w]WhereName ="(\s+|({location_door}[^"]+))""""
  """[^\w]FullName ="(\s+|({full_name}[^"]+))""""
  """[^\w]FirstName ="(\s+|({first_name}[^"]+))""""
  """[^\w]LastName ="(\s+|({last_name}[^"]+))""""
  """[^\w]CardID="(\s+|({badge_id}[^"]+))""""
  """[^\w]CardNumber="(\s+|({employee_id}[^"]+))""""
  """[^\w]EmployeeNumber="(\s+|({employee_id}[^"]+))""""
]
ParserVersion = "v1.0.0"


}
```