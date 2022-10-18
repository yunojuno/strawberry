---
title: Frequently asked questions
---

## Can I reuse Object Types with Input Objects?

Unfortunately not because, as the
[GraphQL spec](https://spec.graphql.org/June2018/#sec-Input-Objects) specifies, there is
a difference between Objects Types and Inputs types:

> The GraphQL Object type (ObjectTypeDefinition) defined above is inappropriate for
> re‐use here, because Object types can contain fields that define arguments or contain
> references to interfaces and unions, neither of which is appropriate for use as an
> input argument. For this reason, input objects have a separate type in the system.

And this is also true for Input types' fields: you can only use Strawberry Input types
or scalar.

See our [Input Types](../types/input-types.md) docs.

## Can I use asyncio with Strawberry and Django?

Yes, we do! Strawberry provides an async view taht you can use with Django 3.1+! Check
[Async Django](../integrations/django.md#async-django) for more information.

## How can I do authentication with Strawberry?

Authentication is a task that should be handled by the framework, and you should check
its documentation about how to do it. Strawberry it's only a wrapper around your
authentication logic.

You should check our [Authentication](../guides/authentication.md) docs to understand
how to deal with authentication with Strawberry, but TL;TR you should define a mutation
that authenticate the user and then use [`Permissions` classes](./permissions.md).
