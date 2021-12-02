# Reproduction of a Renovate issue

https://github.com/renovatebot/renovate/issues/12854

The `core` project has two dependencies:
* `"io.monix:monix_$scalaVersion:$monixVersion"`
* `"com.avast.clients.rabbitmq:rabbitmq-client-extras-scalapb_$scalaVersion:8.6.7"`

The first uses two variables defined in the root project, and it is correctly updated by Renovate.

The second dependency uses just one variable and it is not updated by Renovate. It is possible to fix it by extracting `8.6.7` to a variable (so this is not a problem with a particular dependency).
