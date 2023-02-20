# Kafka Connect NullAwareJsonConverter

NullAwareJsonConverter is same as the JsonConverter one bundled with Kafka, but with updated behavior:
**Any optional field with NULL value stays NULL**.

For more information: [click here](https://cwiki.apache.org/confluence/display/KAFKA/KIP-581%3A+Value+of+optional+null+field+which+has+default+value).

# Usage

Place jar to the `plugin.path` on every Connect worker node.


Provide global configuration options (e.g. `connect-distributed.properties`):
```properties
key.converter=com.oportun.nullawarejson.JsonConverter
value.converter=com.oportun.nullawarejson.JsonConverter
```

Or provide configuration explicitly for Debezium and S3 Sink connectors via Json:
```
...
"key.converter": "com.oportun.nullawarejson.JsonConverter"
"value.converter": "com.oportun.nullawarejson.JsonConverter"
...
```

# Configuration Options

Same as original JsonConverter.
