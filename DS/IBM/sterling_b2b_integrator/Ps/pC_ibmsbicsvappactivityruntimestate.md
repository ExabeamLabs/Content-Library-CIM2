#### Parser Content
```Java
{
Name = ibm-sbi-csv-app-activity-runtimestate
  Conditions = [ """Record adapter runtime state""", """sterling"""]
  ParserVersion = "v1.0.0"

sterling-integrator {
    Vendor = IBM
    Product = Sterling B2B Integrator
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
    Fields = [
      """\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d)\+\d\d:\d\d\s+sterling""",
      """sterling(\s-){3}\s+({host}[^,]+)""",
      """sterling(?:\s-){3}\s+(?:[^,]+,)({sub_category}[^,]+)""",
      """sterling(?:\s-){3}\s+(?:[^,]+,){2}({object}[^,]+)""",
      """sterling(?:\s-){3}\s+(?:[^,]+,){3}({action}[^,]+\w+)""",
      """sterling(?:\s-){3}\s+(?:[^,]+,){4}({description}[^,]+)""",
      """sterling(?:\s-){3}\s+(?:[^,]+,){5}({user_id}[^,]+)""",
    
}
```