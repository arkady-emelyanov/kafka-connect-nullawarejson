# Kafka Connect NullAwareJsonSerializer

WIP.

Isolated implementation of: https://github.com/apache/kafka/pull/12126
Optional NULL fields will stay NULLs.

# Usage

Use Converter in the Debezium Connector configuration:
```
...
"key.converter": "com.oportun.nullawarejson.JsonConverter",
"value.converter": "com.oportun.nullawarejson.JsonConverter",
...
```

Use Converter in the S3 sink Connector configuration:
```
...
"key.converter": "com.oportun.nullawarejson.JsonConverter",
"value.converter": "com.oportun.nullawarejson.JsonConverter",
...
```

# Configuration Options

None.