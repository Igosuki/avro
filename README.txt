Apache Avro™ is a data serialization system.

Learn more about Avro, please visit our website at:

  http://avro.apache.org/

To contribute to Avro, please read:

  https://cwiki.apache.org/confluence/display/AVRO/How+To+Contribute

TODO :
- GenericDatumReader or Writer should iterate over logical types of a union and execute the conversions until one passes.

Stacktrace : 
```
  [org.apache.avro.generic.GenericData getSchemaName GenericData.java 772]
  [org.apache.avro.specific.SpecificData getSchemaName SpecificData.java 302]
  [org.apache.avro.generic.GenericData resolveUnion GenericData.java 737]
  [org.apache.avro.generic.GenericDatumWriter resolveUnion GenericDatumWriter.java 205]
  [org.apache.avro.generic.GenericDatumWriter writeWithoutConversion GenericDatumWriter.java 123]
  [org.apache.avro.specific.SpecificDatumWriter writeField SpecificDatumWriter.java 87]
  [org.apache.avro.generic.GenericDatumWriter writeRecord GenericDatumWriter.java 156]
  [org.apache.avro.generic.GenericDatumWriter writeWithoutConversion GenericDatumWriter.java 118]
  [org.apache.avro.generic.GenericDatumWriter write GenericDatumWriter.java 75]
  [org.apache.avro.generic.GenericDatumWriter write GenericDatumWriter.java 62]
```
