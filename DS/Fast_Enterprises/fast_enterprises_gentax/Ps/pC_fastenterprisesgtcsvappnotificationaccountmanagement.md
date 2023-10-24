#### Parser Content
```Java
{
Name = fastenterprises-gt-csv-app-notification-accountmanagement
 ParserVersion = v1.0.0
 Vendor = Fast Enterprises
 Product = Fast Enterprises GenTax
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [ """,WEB.GENTAX,""", """,AccountManagement,""" ]
 Fields = [
   """({app}WEB\.GENTAX),({event_category}AccountManagement)""",
   """AccountManagement,({category}[^,]+),({event_code}\d+),({account_id}[^,]+),({account}[^,]+),({user_id}[^,]+),({user}[\w\.\-]{1,40}\$?),({user_type}[^,]+),({operation}[^,]+),({additional_info}[^,]+?)\s*$"""
 ]
 DupFields = [ "account->object" ]


}
```