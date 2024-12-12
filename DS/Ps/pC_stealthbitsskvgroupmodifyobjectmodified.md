#### Parser Content
```Java
{
Name = stealthbits-s-kv-group-modify-objectmodified
  ParserVersion = "v1.0.0"
  Conditions = [ """StealthINTERCEPT""", """Object Modified""", """ObjectClass="group"""", """ SuccessfulChange="""" ]
  Fields = ${StealthBitsParsersTempletes.stealthintercept-ad-events.Fields} [
    """\sDistinguishedName ="CN=.+?,({group_ou}OU.+?DC=.+?)""""
  ]


}
```