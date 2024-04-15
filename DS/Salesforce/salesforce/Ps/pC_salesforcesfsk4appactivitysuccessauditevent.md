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
"""CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
"""suser=(({domain}[^\\\s@;=]+)\\+)?(system|({user}[^\\\=\s;@]+))\s+(\w+=|$)"""
"""suser=({email_address}[^\\\=\s;@]+@[^\\\=\s;@]+)"""
"""user\s+({email_address}[^@]+@[^\.]+\.[^\]\s",\|]+),\s"""
"""Owner\.Name\\=(System|({full_name}[^;]+?));"""
""";Name\\=({object}[^;]+?);"""
"""dproc=({operation}[^;]+?)\s+(\w+=|$)"""
""";Action\\=({operation}[^;]+)"""
"""ACTION_MESSAGE\\?=({additional_info}[^;]+)"""
"""Display\\=({additional_info}.+?)\s*(\w+=|$)"""
"""({app}Sales Cloud)"""
"""CLIENT_IP\\=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""USER_TYPE\\?=({user_type}[^;]+)"""
"""USER_AGENT\\?=({user_agent}[^\n]+?);REQUEST_METHOD"""
"""REQUEST_METHOD\\?=({method}[^;]+),Action\\=({operation}[^;]+)"""
]
ParserVersion = "v1.0.0"


}
```