# Kafka Connect NullAwareJsonConverter

Isolated implementation of: https://github.com/apache/kafka/pull/12126
Optional NULL fields will stay NULLs.

# Usage

Place jar to the Connect `plugin.path`.

Update Debezium connector configuration as following:
```
...
"key.converter": "com.oportun.nullawarejson.JsonConverter",
"value.converter": "com.oportun.nullawarejson.JsonConverter",
...
```

Update S3 sink connector configuration as following:
```
...
"key.converter": "com.oportun.nullawarejson.JsonConverter",
"value.converter": "com.oportun.nullawarejson.JsonConverter",
...
```

# Configuration Options

Same as original JsonConverter.
