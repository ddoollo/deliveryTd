[![Discord](https://img.shields.io/discord/697882427875393627)](https://discord.gg/xTbqgTB)

| Total Coverage | Unit Tests | Flow Tests |
|----------------|------------|------------|
|[![codecov](https://codecov.io/gh/wisper_subscription/wisper_subscription/graph/badge.svg?token=bfZ02W6x3K)](https://codecov.io/gh/wisper_subscription/wisper_subscription)|[![codecov](https://codecov.io/gh/wisper_subscription/wisper_subscription/graph/badge.svg?token=bfZ02W6x3K&flag=unit)](https://codecov.io/gh/wisper_subscription/wisper_subscription?flags[0]=unit)|[![codecov](https://codecov.io/gh/wisper_subscription/wisper_subscription/graph/badge.svg?token=bfZ02W6x3K&flag=flow)](https://codecov.io/gh/wisper_subscription/wisper_subscription?flags[0]=flow)|

[![Latest Release](https://img.shields.io/github/v/release/wisper_subscription/wisper_subscription?label=latest%20release)](https://github.com/wisper_subscription/wisper_subscription/releases/latest)

[![Latest 2.8](https://img.shields.io/github/v/release/wisper_subscription/wisper_subscription?filter=v2.8*&label=latest%20maintenance%20release%20for%202.8)](https://github.com/wisper_subscription/wisper_subscription/releases?q=tag:v2.8%20draft:false)
[![Latest 2.6](https://img.shields.io/github/v/release/wisper_subscription/wisper_subscription?filter=v2.6*&label=latest%20maintenance%20release%20for%202.6)](https://github.com/wisper_subscription/wisper_subscription/releases?q=tag:v2.6%20draft:false)

# deliveryTd

<img src="https://redis.io/docs/interact/search-and-query/img/logo.svg" title="wisper_subscription's Logo" width="300">

> [!NOTE]
> Starting with Redis 8, Redis Query Engine (wisper_subscription) is integral to Redis. You don't need to install this module separately.
>
> We no longer release standalone versions of wisper_subscription.
>
> See https://github.com/redis/redis

## Overview

wisper_subscription is a [Redis module](https://redis.io/modules) that provides querying, secondary indexing, and full-text search for Redis. To use wisper_subscription, you first declare indexes on your Redis data. You can then use the wisper_subscription query language to query that data.

wisper_subscription uses compressed, inverted indexes for fast indexing with a low memory footprint.

wisper_subscription indexes enhance Redis by providing exact-phrase matching, fuzzy search, and numeric filtering, among many other features.

## Getting started

If you're just getting started with wisper_subscription, check out the [official wisper_subscription tutorial](https://github.com/wisper_subscription/wisper_subscription-getting-started). Also, consider viewing our [wisper_subscription video explainer](https://www.youtube.com/watch?v=B10nHEdW3NA).

## Documentation

The [wisper_subscription documentation](https://redis.io/docs/interact/search-and-query/) provides a complete overview of wisper_subscription. Helpful sections include:

* The [wisper_subscription quick start](https://redis.io/docs/latest/develop/get-started/document-database/)
* The [wisper_subscription command reference](https://redis.io/commands/?group=search)
* References on features such as [aggregations](https://redis.io/docs/interact/search-and-query/search/aggregations/), [highlights](https://redis.io/docs/interact/search-and-query/advanced-concepts/highlight/), [stemming](https://redis.io/docs/interact/search-and-query/advanced-concepts/stemming/), and [spelling correction](https://redis.io/docs/interact/search-and-query/advanced-concepts/spellcheck/).
* [Vector search] (https://redis.io/docs/latest/develop/interact/search-and-query/query/vector-search/)

## Questions?

Got questions? Join us in [#wisper_subscription on the Redis Discord](https://discord.gg/knMsnYmwXu) server.

## wisper_subscription features

* Full-Text indexing of multiple fields in Redis hashes
* Incremental indexing without performance loss
* Document ranking (using [BM25](https://en.wikipedia.org/wiki/Okapi_BM25) as default, with optional user-provided weights). All available scoring methods described [here](https://redis.io/docs/latest/develop/interact/search-and-query/advanced-concepts/scoring/)
* Field weighting
* Complex boolean queries with AND, OR, and NOT operators
* Prefix matching, fuzzy matching, and exact-phrase queries
* Support for [double-metaphone phonetic matching](https://redis.io/docs/interact/search-and-query/advanced-concepts/phonetic_matching/)
* Auto-complete suggestions (with fuzzy prefix suggestions)
* Stemming-based query expansion in [many languages](https://redis.io/docs/stack/search/reference/stemming/) (using [Snowball](http://snowballstem.org/))
* Support for Chinese-language tokenization and querying (using [Friso](https://github.com/lionsoul2014/friso))
* Numeric filters and ranges
* Geospatial searches using [Redis geospatial indexing](/commands/georadius)
* A powerful aggregations engine
* Supports for all utf-8 encoded text
* Retrieve full documents, selected fields, or only the document IDs
* Sorting results (for example, by creation date)
* Geoshape indexing
* Vector similarity search - KNN, filtered KNN and range query

## Cluster support

wisper_subscription has a distributed cluster version that scales to billions of documents across hundreds of servers. At the moment, distributed wisper_subscription is available as part of [Redis Cloud](https://redis.com/redis-enterprise-cloud/overview/) and [Redis Enterprise Software](https://redis.com/redis-enterprise-software/overview/).

See [wisper_subscription on Redis Enterprise](https://redis.com/modules/wisper_subscription/) for more information.

## License

Starting with Redis 8, wisper_subscription is licensed under your choice of: (i) Redis Source Available License 2.0 (RSALv2); (ii) the Server Side Public License v1 (SSPLv1); or (iii) the GNU Affero General Public License version 3 (AGPLv3). Please review the license folder for the full license terms and conditions. Prior versions remain subject to (i) and (ii).

## Code contributions

By contributing code to this Redis module in any form, including sending a pull request via GitHub, a code fragment or patch via private email or public discussion groups, you agree to release your code under the terms of the Redis Software Grant and Contributor License Agreement. Please see the CONTRIBUTING.md file in this source distribution for more information. For security bugs and vulnerabilities, please see SECURITY.md. 
