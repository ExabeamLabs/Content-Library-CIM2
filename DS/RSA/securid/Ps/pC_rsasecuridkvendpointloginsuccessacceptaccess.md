#### Parser Content
```Java
{
Name = "rsa-securid-kv-endpoint-login-success-acceptaccess"
Vendor = "RSA"
Product = "SecurID"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
""" SINGLEPOINT """
""" RADIUS_USER_TOKENCODE_AUTHENTICATION """
"""RADIUS_RESPONSE_TYPE="Access-Accept""""
"""STATUS="SUCCESS""""
]
Fields = [
"""({host}[^\s]+)\s\S+\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""DESCRIPTION="({additional_info}[^".]+)"""
"""SOURCE-IP-ADDRESS="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""USER_NAME="({user}[^"]+)"""
"""POLICY_ID="({policy_name}[^"]+)"""
"""STATUS="({result}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```