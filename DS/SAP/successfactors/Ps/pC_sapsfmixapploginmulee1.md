#### Parser Content
```Java
{
Name = sap-sf-mix-app-login-mulee-1
  Conditions = [ """action=login""", """ mule_ee """, """ SuccessFactors """ ]
  ParserVersion = "v1.0.0"

sap-successfactors-activity = {
    Vendor = SAP
    Product = SuccessFactors
    TimeFormat = "yyyy-MM-dd'T'HH.mm.ss.SSSZ"
    Fields = [
      """"Time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d\.\d\d\.\d\d\.\d\d\dZ)"""",
      """"Host":\s*"({host}[\w.-]+)"""",
      """sourceip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """action=({event_name}[^,]+)""",
      """({app}SuccessFactors)""",
      """state=({result}[^,]+)""",
      """"Account":\s*"({account}[^"]+)""",
      """severity=({severity}[^,]+)""",
      """objectType=((N\/A)|({object_type}[^,]+))""",
      """objectId=\\?"({object_id}[^\\"]+)""",
      """category=({category}[^,]+)""",
      """correlationId=({correlation_id}[^,]+)""",
# caller is removed
    
}
```