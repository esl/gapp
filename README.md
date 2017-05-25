Gapp
=====

Generic application template

Build
-----

    $ rebar3 compile

Gapp
----

This template is to be used to initiate a new application that needs the
following default functionality:

- Configuration management (cfg)
= Logging (olog)
- Application analysis (sappan)

The respective applications are to be found in their own repositories.

Gapp itself provides meck (a mocking library for tests) and proper
(property based testing) when tests are run.

Architecture
------------

Gapp sets up an application that can be used in an Erlang cluster where all
nodes are connected. All application based on gapp will inherit common logging,
configuration management, application upgrade analysis and utilities.

When a gapp based application starts, it first shall connect to an Erlang
cluster, then starts the cfg (config) app, then the logger.

This also means, the cfg application shall use its on logging
to debug itself when needed.

