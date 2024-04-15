#### Parser Content
```Java
{
Name = "salesforce-sf-kv-app-login-login"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""SFDCLogType=""""
"""SFDCLogId=""""
"""EVENT_TYPE="Login""""
]
Fields = [
"""SFDCLogDate="({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d.\d\d\d(\-|\+)\d+)"""
"""BROWSER_TYPE="({user_agent}[^"]+)"""
"""TLS_PROTOCOL="({protocol}[^"]+)"""
"""SOURCE_IP="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""USER_ID="({user}[^"\s]+)"""
"""LOGIN_STATUS="({result}[^"]+)"""
"""USER_NAME="({email_address}[^"@]+@({email_domain}[^\s";]+))""""
]
ParserVersion = "v1.0.0"


}
```