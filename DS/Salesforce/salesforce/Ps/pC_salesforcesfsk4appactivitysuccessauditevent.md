#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-auditevent"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""destinationServiceName =Sales Cloud"""
"""|audit-event|"""
]
Fields = [
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""
"""CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""LastModifiedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""CreatedBy\.Username\\=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
"""suser=(({domain}[^\\\s@;=]+)\\+)?(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)"""
"""suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
"""user\s+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)),\s"""
"""Owner\.Name\\?=({full_name}({first_name}[^\s]+)\s({last_name}[^;]+))"""
""";Name\\=({object}[^;]+?);"""
"""dproc=({operation}[^;]+?)\s+(\w+=|$)"""
""";Action\\=({operation}[^;]+)"""
"""ACTION_MESSAGE\\?=({additional_info}[^;]+)"""
"""Display\\=({additional_info}.+?)\s*(\w+=|$)"""
"""({app}Sales Cloud)"""
"""CLIENT_IP\\=({assigned_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""SOURCE_IP\\=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""USER_TYPE\\?=({user_type}[^;]+)"""
"""USER_AGENT\\?=({user_agent}[^\n]+?);REQUEST_METHOD"""
"""REQUEST_METHOD\\?=({method}[^;]+),Action\\=({operation}[^;]+)""",
"""REQUEST_METHOD\\?=({method}[^;]+)""",
"""OS_NAME\\?=({os}[^;]+)""",
"""DEVICE_ID\\?=({device_id}[^;]+)""",
"""BROWSER_NAME\\?=({browser}[^;]+)""",
"""CLIENT_GEO\\?=({src_country}[^;/]+)"""
]
ParserVersion = "v1.0.0"
DupFields = [ "full_name->username" ]


}
```