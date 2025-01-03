---
id: samples-rust
title: Rust GraphQL Application
sidebar_label: Rust + Mongo (GraphQL)
description: The following sample app to test Keploy integration capabilities using rust and MongoDb.
tags:
  - Rust
  - MongoDB
  - GraphQL
keyword:
  - Rust
  - MongoDB
  - GraphQL
  - API Test generator
  - Auto Testcase generation
---

<head>
  <title> Rust + Mongo (GraphQL) | Keploy Docs</title>
  <meta charSet="utf-8" />
</head>

## Introduction

This is a sample app to test Keploy integration capabilities using rust and MongoDb. Buckle up, it's gonna be a fun ride! 🎢

## Install Keploy CLI 🚀

Get Started with One-Click Command: -

```bash
 curl -O -L https://keploy.io/install.sh && source install.sh
```

Or, you can follow the detailed instructions [here](https://keploy.io/docs/server/installation/). 🎉 Wohoo! We are all set to use Keploy.

## Get Started! 🎬

## Setup app

Now that we have bun installed, we will setup our application.

```bash
git clone https://github.com/keploy/samples-rust && cd samples-rust/gql-mongo
```

## Running App Locally on Linux/WSL 🐧

We will be using Docker compose to run Mongo on Docker container.

### Let's start the MongoDB Instance

```zsh
docker compose up -d
```

### Capture testcase

```bash
sudo -E env PATH=$PATH keploy record -c 'cargo run'
```

#### Generate testcase

Go to the http://127.0.0.1:8000 and create some queries.

We will get the following output in our terminal

![Test-case](/img/rust-mongo-test-case.png?raw=true)

### Run the testcases

Now, let's run the keploy in test mode again:-

```bash
sudo -E env PATH=$PATH keploy test -c 'cargo run'
```

![TestRun](/img/rust-mongo-test-run.png?raw=true)

_Voila!! Our testcases has passed 🌟_

Hope this helps you out, if you still have any questions, reach out to us .

import GetSupport from '../concepts/support.md'

<GetSupport/>
