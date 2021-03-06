# avlizer - Avro Serializer for Erlang

`avlizer` is built on top of [erlavro](https://github.com/klarna/erlavro)
The design goal of this application is to provide APIs for users to serialize
or deserialize data with minimal overhead of schema management.

# Integrations

## Confluent Schema Registry

[Confluent schema registry](https://github.com/confluentinc/schema-registry)
provides REST APIs for schema registration and lookups.

### Config
Make sure schema registry URL is present in `sys.config` as below

```
{avlizer, [{avlizer_confluent, #{schema_registry_url => URL}}]}
```

Or set os env variable: `AVLIZER_CONFLUENT_SCHEMAREGISTRY_URL`

