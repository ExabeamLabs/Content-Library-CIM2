#### Parser Content
```Java
{
Name = google-cloudplatform-json-app-database-success-database
  Vendor = Google
  Product = Google Cloud Platform
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [""""database_id":"""",  """"type":"cloudsql_database"""",""""project_id":"""","""dproc=Cloud PubSub"""]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """"service_name":"({service_name}[^"]+)"""",
    """destinationServiceName =({app}[^=]+?)\s\w+=""",
	  """"region":"({region}[^"]+)"""",
	  """STATEMENT:\s*({db_query}[^;]+)""",
	  """user\\?=({db_user}[^\s]+)""",
	  """db\\?=({db_name}[^\s,]+)"""
  ]
  ParserVersion = v1.0.0


}
```