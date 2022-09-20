#### Parser Content
```Java
{
Name = sap-sf-mix-app-authentication-success-authenticate
  Conditions = [ """action=authenticate""", """ mule_ee """, """ SuccessFactors """ ]
  ParserVersion = "v1.0.0"

sap-successfactors-activity = {
    Vendor = SAP
    Product = SuccessFactors
    TimeFormat = "yyyy-MM-dd'T'HH.mm.ss.sssZ"
    Fields = [
      """"Time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d\.\d\d\.\d\d\.\d\d\dZ)"""",
      """"Host":\s*"({host}[\w.-]+)"""",
      """sourceip="({src_ip}[\da-fA-F.:]+)"""",
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