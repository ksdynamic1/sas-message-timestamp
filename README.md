# RabbitMQ Message Timestamp Plugin 

This plugin fills the `timestamp_in_ms` and `timestamp_in_ns` headers of a message as it enters
RabbitMQ with the current (server node) timestamp value.

## Supported Versions 

This plugin targets RabbitMQ 3.6.0 until 3.11.

This plugin requires Ubuntu 20.04 along with Erlang 25.3 and Elixir 1.14.5-otp-25.

## Limitations

This plugin cannot be used together with [rabbitmq-routing-node-stamp](https://github.com/rabbitmq/rabbitmq-routing-node-stamp)
as they override the same extension point.

## Building from Source

1. Ensure `Erlang 25.3` and `Elixir 1.14.5-otp-25` is present on `Ubuntu 20.04` system
2. Clone repository and enter the folder
3. Make the project
```
make query-deps
make
DIST_AS_EZS=yes make dist
```
4. Enter the `plugins` folder to see the `rabbitmq_message_timestamp-v3.11.x.ez` plugin for RabbitMQ 

## Resources 

- [Install Erlang and Elixir Ubuntu 20.04](https://alexanderzeitler.com/articles/installing-latest-elixir-erlang-version-on-xubuntu-ubuntu-lts-22.04-asdf/)