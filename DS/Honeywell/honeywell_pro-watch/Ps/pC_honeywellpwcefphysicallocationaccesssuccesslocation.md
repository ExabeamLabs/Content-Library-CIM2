#### Parser Content
```Java
{
Name = "honeywell-pw-cef-physical-location-access-success-location"
Vendor = "Honeywell"
Product = "Honeywell Pro-Watch"
TimeFormat = "epoch"
Conditions = [
  """|ProWatch|Access System|"""
  """cs6Label=Location"""
  """ cs4="""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\|ProWatch\|Access System\|([^\|]*\|){2}({result}[^\|]+)\|"""
  """\sduser=\s*({last_name}[^,]+?)\s*,\s*({first_name}.+?)\s+\w+="""
  """\scs6=\s*(Empty|({location_door}\S.*?))\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```